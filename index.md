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