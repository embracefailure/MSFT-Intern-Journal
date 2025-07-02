---
layout: page
title: 项目展示
permalink: /projects/
---

# 前言

这里记录我在微软实习期间参与的项目、使用的技术和实现的成果。

---

## MCP 协议 Agent 能力复现项目

在实习期间，我深入研究了 **Model Context Protocol (MCP)** 协议，并成功把3个不同的MCP server与Agent连接，展示了MCP如何帮助快速开发智能体，实现自然语言与软件系统，内部技术文档，以及浏览器的无缝交互的效果。

### 🎬 项目演示视频

<div style="text-align: center; margin: 20px 0;">
  <video width="100%" max-width="800px" controls>
    <source src="assets/videos/Blender_demo.mp4" type="video/mp4">
    您的浏览器不支持视频播放。
  </video>
  <p><em>Blender MCP + Claude Desktop</em></p>
</div>
<div style="text-align: center; margin: 20px 0;">
  <video width="100%" max-width="800px" controls>
    <source src="assets/videos/Playwright_demo.mp4" type="video/mp4">
    您的浏览器不支持视频播放。
  </video>
  <p><em>Playwright MCP + GitHub Copilot</em></p>
</div>

### 📋 项目概览

| 项目 | 技术栈 | 实现功能 | 状态 |
|------|--------|----------|------|
| **Blender MCP Agent** | Blender MCP Server + Claude Desktop | 自然语言控制3D渲染软件 | ✅ 完成 |
| **Microsoft Docs Agent** | Microsoft Docs MCP Server + GitHub Copilot | 自然语言精准查询微软技术文档 | ✅ 完成 |
| **Web Automation Agent** | Playwright MCP Server + GitHub Copilot | 自然语言控制网页自动化操作 | ✅ 完成 |

---

### 🎨 项目一：Blender MCP Agent

**技术实现：** Blender MCP Server + Claude Desktop

**项目描述：**
通过 MCP 协议连接 Blender 3D 软件与 Claude AI，实现了用自然语言直接控制 3D 建模和渲染操作。用户可以通过对话的方式创建 3D 对象、调整材质、设置灯光和渲染场景。

**主要功能：**
- 🎯 自然语言创建和编辑 3D 对象
- 🎨 智能材质和纹理应用
- 💡 动态灯光设置和调整
- 📸 自动渲染和导出功能

**技术亮点：**
- 实现了复杂 3D 操作的语义解析
- 建立了稳定的 MCP 通信机制
- 提供了直观的创作工作流

---

### 📚 项目二：Microsoft Docs Agent

**技术实现：** Microsoft Docs MCP Server + GitHub Copilot

**项目描述：**
构建了一个能够精准查询微软技术文档的智能助手。通过 MCP 协议集成微软官方文档数据源，让开发者能够通过自然语言快速找到准确的技术信息和代码示例。

**主要功能：**
- 🔍 智能文档内容检索
- 📖 上下文相关的技术解答
- 💻 相关代码示例推荐
- 🔗 精准的文档链接定位

**技术亮点：**
- 高效的文档索引和检索算法
- 语义理解与技术内容匹配
- 实时的文档更新同步机制

---

### 🌐 项目三：Web Automation Agent

**技术实现：** Playwright MCP Server + GitHub Copilot

**项目描述：**
开发了一个能够理解自然语言指令并自动执行网页操作的智能代理。用户只需描述想要完成的任务，Agent 就能自动识别页面元素并执行相应的点击、输入、导航等操作。

**主要功能：**
- 🖱️ 智能页面元素识别和操作
- ⌨️ 自动表单填写和提交
- 🧭 智能页面导航和跳转
- 📊 操作结果验证和反馈

**技术亮点：**
- robust 的页面元素定位策略
- 自然语言到操作指令的转换
- 异常处理和错误恢复机制

---

### 🎯 项目总结

这三个项目展示了 MCP 协议在不同应用场景下的强大能力：

1. **创意软件集成** - 降低了专业软件的使用门槛
2. **知识管理优化** - 提升了技术文档的查询效率  
3. **自动化流程简化** - 让复杂的网页操作变得简单直观

通过这些项目的实践，我深入理解了：
- MCP 协议的设计理念和实现机制
- 自然语言处理在实际应用中的挑战和解决方案
- 人机交互界面的未来发展趋势

---

### 🔗 相关资源

- [MCP 协议官方文档](https://modelcontextprotocol.io/)
- [MCP Server仓库](https://mcp.so/servers)
<!--- [项目源代码仓库](#) <!-- 添加你的 GitHub 链接 -->
<!--- [技术博客详解](/tech/) <!-- 链接到技术学习页面 -->

---

*最后更新：2025年7月*