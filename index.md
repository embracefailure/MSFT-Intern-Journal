---
layout: default
title: 首页
permalink: /
---

# Hi

欢迎来到我的实习记录网站！这里将持续更新我在微软实习期间的技术学习、项目经验、行业认知与思考。

## 实习概览

- Role：Account Tech Strategist
- Mentor：Mingqi Shan
- Location：深圳
- Time：2025年6月起

## 踩坑记录

- 发现我的Azure订阅不能开域名，卡在验证那一步，说没有配额可以开，可能的原因是账户类型是MSDN,不支持我开域名服务，Azure学生账户也不行。
- 上传GitHub的视频尽量压缩到100Mb以下，否则会需要lfs处理。
- 视频路径最好写绝对路径，不然就用开发者工具检查下路径为什么不对。

- multi agent环境需要装docker desktop，这时候已经可以在任务资源管理器看到CPU虚拟化enabled，但是docker报错
    ```
    HCS_E_SERVICE_NOT_AVAILABLE
    "The operation could not be started because a required feature is not installed."
    ```
    解决方法：
    在powershell里面运行命令：

    ```powershell
        dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
        dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
        dism.exe /online /enable-feature /featurename:Microsoft-Hyper-V-All /all /norestart
    ```

    然后重启电脑。

- 按照我使用azd up命令后，报错配额不够。设置location为eastus后仍然不行。

- 使用check quota.sh文件查看配额，发现我的60开头的订阅没有Azure openai配额。另一个有。另一个TPM的限制是50K，符合文档里面MSDN型订阅的限制。于是用：https://aka.ms/oai/stuquotarequest 提升配额到140K。同时，我发现有人遇到过这个问题： https://github.com/microsoft/Multi-Agent-Custom-Automation-Engine-Solution-Accelerator/issues/257

- 使用微软另一个仓库就可以满足限额要求：https://github.com/Azure-Samples/get-started-with-ai-agents/tree/main?tab=readme-ov-file#deploying-steps 
但是架构不同，这个是单一agent，能基于上传文件检索。但是不能联网搜索。UI找不到上传文件的位置，应该是前端没有写上传文件的按钮。

- 可以确定截止2025年7月10日，m365 copilot和copilot studio并不支持连接researcher agent到别的agent上。Azure AI Foundry不支持创建基于reasoning模型的agent。但是copilot studio可以通过打开设置里面的reasoning，并在agent的instructions里面对需要reasoning的地方进行reasoning，来实现reasoning的功能。

- copilot studio的 topics主要用来引导对话进入不同的处理分支，与我的需求不符合。