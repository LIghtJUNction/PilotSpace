<div align="center">

# 🚀 PilotSpace

**AI原生的工作区革命**

[![License](https://img.shields.io/badge/license-GPLv3-blue.svg)](../LICENSE)
[![Python](https://img.shields.io/badge/python-3.14+-blue.svg)](https://www.python.org/)
[![Status](https://img.shields.io/badge/status-开发中-yellow.svg)]()

[English](README.md) | 简体中文

---

*一个深度集成人工智能的现代化 Linux 桌面环境配置方案*

</div>

## 📑 目录

- [✨ 特性](#-特性)
- [🎯 项目目标](#-项目目标)
- [🛠️ 技术栈](#️-技术栈)
- [📦 安装](#-安装)
  - [系统要求](#系统要求)
  - [安装步骤](#安装步骤)
- [🎨 自定义](#-自定义)
- [📂 项目结构](#-项目结构)
- [🔧 预配置软件](#-预配置软件)
- [❓ 常见问题](#-常见问题)
- [🤝 贡献](#-贡献)
- [🌿 分支维护](#-分支维护)
- [💡 致谢](#-致谢)
- [📄 许可证](#-许可证)

## ✨ 特性

🚧 **项目状态：开发中** - 我们正在积极开发新功能和改进

- 🤖 **AI 深度集成** - 将大语言模型无缝集成到桌面环境中
- 🎨 **现代化 UI** - 基于 Hyprland 和 quickshell 的创新界面设计
- ⚙️ **灵活配置** - 使用 yolk 管理，轻松定制你的工作区
- 📦 **预配置优化** - 大量常用软件的开箱即用配置
- 🔄 **模块化设计** - 通过 yolk.rhai 自由组合你喜欢的工具

## 🎯 项目目标

PilotSpace 旨在创建一个革命性的工作空间，具体目标包括：

- 🧠 **深度集成大语言模型** - 让 AI 成为你的桌面助手
- 🎨 **创新的界面设计** - 独特、现代、高效的用户体验
- ⚡ **高性能体验** - 基于 Hyprland Wayland 合成器
- 🔧 **智能配置管理** - 使用 yolk 实现优雅的 dotfiles 管理
- 🌐 **开放生态** - 支持多种工具链和工作流

## 🛠️ 技术栈

| 组件 | 技术选型 | 说明 |
|------|---------|------|
| 🐚 **Shell** | Zsh | 默认 shell 环境 |
| 🪟 **窗口管理器** | Hyprland | 现代化的 Wayland 合成器 |
| 🎛️ **状态栏/面板** | quickshell | 灵活的桌面组件 |
| 💻 **终端模拟器** | Kitty | GPU 加速的高性能终端 |
| ⚙️ **配置管理** | yolk | 强大的 dotfiles 管理工具 |
| 🐍 **开发语言** | Python 3.14+ | 核心功能开发 |

## 📦 安装

### 系统要求

- Linux 操作系统（推荐 Arch Linux 或其衍生版）
- Python 3.14 或更高版本
- 支持 Wayland 的显示服务器
- 基本的开发工具链

### 安装步骤

本项目使用 **yolk** 管理配置文件，安装过程如下：

#### 1. 安装依赖软件

首先确保安装了所有必需的依赖包：

```bash
# Arch Linux / Manjaro
sudo pacman -S hyprland kitty zsh yolk

# 其他发行版请参考各组件官方文档
```

#### 2. 配置 yolk

使用 yolk 绑定到 pilotspace-eggs 配置仓库：

```bash
# 配置 yolk
yolk init
```

#### 3. 拉取并同步配置

```bash
# 拉取配置文件
yolk pull

# 同步配置到系统
yolk sync
```

#### 4. 应用配置

重新登录或重启系统以应用新的桌面环境配置。

## 🎨 自定义

### 如何保留自定义配置？

PilotSpace 设计为完全可定制的工作区，推荐的自定义方法：

1. **Fork 本仓库** 🍴
   - 在 GitHub 上 fork `PilotSpace` 仓库
   - 这样你可以保留自己的修改并追踪上游更新

2. **按需修改配置** ✏️
   - 编辑 `yolk.rhai` 文件来启用/禁用模块
   - 修改 `PilotSpace-eggs` 中的配置文件
   - 调整主题、快捷键、工作流等

3. **保持更新** 🔄
   - 定期从上游仓库拉取更新
   - 合并新功能到你的 fork 中

### 配置文件结构

```
PilotSpace/
├── yolk.rhai              # yolk 配置文件
├── PilotSpace-eggs/       # 配置文件集合
│   ├── hyprland/         # Hyprland 配置
│   ├── kitty/            # Kitty 配置
│   ├── zsh/              # Zsh 配置
│   └── ...
└── src/                   # Python 源代码
```

## 📂 项目结构

### pilotspace-eggs

这是配置文件的核心子项目：

- 📁 **配置文件集合** - 所有预配置的软件设置都在这里
- 🎨 **UI 设计资源** - 主题、图标、壁纸等设计资源
- 🔧 **模板文件** - 可复用的配置模板

### pilotspace

主项目仓库：

- 📦 **软件包发布** - 本项目的 Python 包将在此发布
- 🤖 **AI 功能模块** - 包含与人工智能相关的 Python 项目
- 🔌 **插件系统** - 扩展和集成功能

## 🔧 预配置软件

本项目计划为以下常见软件提供预配置：

- ✅ **Shell**: Zsh + Oh My Zsh / Powerlevel10k
- ✅ **终端**: Kitty (GPU 加速)
- ✅ **窗口管理器**: Hyprland (Wayland)
- ✅ **面板**: quickshell
- 🔄 **编辑器**: Neovim (计划中)
- 🔄 **文件管理器**: Thunar / ranger (计划中)
- 🔄 **浏览器配置**: Firefox / Chromium (计划中)
- 🔄 **开发工具**: Git, tmux, lazygit (计划中)

通过编辑 `yolk.rhai` 文件，你可以自由选择启用哪些预配置组合。

## ❓ 常见问题

### 为什么选择 yolk？

yolk 的作者同时也是 eww 的作者。在浏览 eww 仓库时发现了这个工具，经过实际体验，发现它确实非常好用：

- ✨ **高级功能** - 支持模板、条件配置等功能
- 🔄 **方便更新** - 轻松管理和同步配置文件
- 📦 **模块化** - 灵活的配置组合方式
- 🎯 **专为 dotfiles 设计** - 针对性强，使用简单

**其他替代品：**
- [dotfiles 管理工具汇总](https://dotfiles.github.io/tutorials/)
- GNU Stow
- chezmoi
- yadm

### 不同组合如何切换？

安装配置文件就像"孵蛋"一样简单：

```bash
# 编辑 yolk.rhai 文件，启用/禁用模块
vim yolk.rhai

# 重新同步配置
yolk sync
```

更新 `yolk.rhai` 文件即可轻松禁用或启用不同的配置组合！

### 支持哪些 Shell？

默认使用 **Zsh**，但我们欢迎社区维护其他 Shell 的分支：

- 🐟 **Fish shell** - 欢迎维护者
- 🐚 **Bash** - 欢迎维护者
- ⚡ **其他 Zsh 框架** - 如 prezto, zinit 等

## 🤝 贡献

我们热烈欢迎各种形式的贡献！

### 如何贡献？

1. 🔍 **提交 Issue** - 报告 bug 或提出新功能建议
2. 🔧 **提交 Pull Request** - 直接贡献代码或配置
3. 📝 **改进文档** - 帮助完善使用说明
4. 🌐 **翻译** - 帮助翻译文档到其他语言

### 贡献指南

```bash
# 1. Fork 本仓库
# 2. 创建特性分支
git checkout -b feature/your-feature-name

# 3. 提交你的修改
git commit -am "Add some feature"

# 4. 推送到分支
git push origin feature/your-feature-name

# 5. 创建 Pull Request
```

请确保你的代码符合项目规范，并添加适当的说明。

## 🌿 分支维护

我们非常欢迎社区维护不同配置方案的分支！

### 欢迎的分支类型

- 🐟 **Fish Shell 版本** - 使用 Fish 替代 Zsh
- ⚡ **不同 Zsh 框架** - 如 prezto, zinit, antigen
- 📝 **不同 Neovim 配置** - 如 LunarVim, NvChad, AstroVim
- 🪟 **其他窗口管理器** - 如 Sway, i3
- 🎨 **不同主题风格** - 暗色/亮色主题变体
- 🖥️ **桌面环境版本** - GNOME/KDE 扩展

如果你维护了一个分支，请通过 Issue 或 PR 告诉我们，我们会在文档中列出！

## 💡 致谢

### 特别感谢

- 🌟 **[end-4/dots-hyprland](https://github.com/end-4/dots-hyprland)** - 感谢 end_4 提供的优秀 Hyprland 配置灵感
- 🛠️ **[yolk](https://github.com/elkowar/yolk)** - 感谢 elkowar 开发的强大配置管理工具
- 🪟 **[Hyprland](https://hyprland.org/)** - 现代化的 Wayland 合成器
- 💻 **[Kitty](https://sw.kovidgoyal.net/kitty/)** - 优秀的 GPU 加速终端

### 社区贡献者

感谢所有为 PilotSpace 做出贡献的开发者和用户！

## 📄 许可证

本项目采用 **GNU General Public License v3.0** 许可证。

详细信息请查看 [LICENSE](../LICENSE) 文件。

---

<div align="center">

**由 ❤️ 和 AI 驱动**

如果这个项目对你有帮助，请给我们一个 ⭐️ 

[报告问题](https://github.com/LIghtJUNction/PilotSpace/issues) · [功能建议](https://github.com/LIghtJUNction/PilotSpace/issues) · [讨论交流](https://github.com/LIghtJUNction/PilotSpace/discussions)

</div>