<div align="center">

# 🚀 PilotSpace

**The AI-Native Workspace Revolution**

[![License](https://img.shields.io/badge/license-GPLv3-blue.svg)](../LICENSE)
[![Python](https://img.shields.io/badge/python-3.14+-blue.svg)](https://www.python.org/)
[![Status](https://img.shields.io/badge/status-in%20development-yellow.svg)]()

English | [简体中文](README_CN.md)

---

*A modern Linux desktop environment configuration deeply integrated with artificial intelligence*

</div>

## 📑 Table of Contents

- [✨ Features](#-features)
- [🎯 Project Goals](#-project-goals)
- [🛠️ Tech Stack](#️-tech-stack)
- [📦 Installation](#-installation)
  - [System Requirements](#system-requirements)
  - [Installation Steps](#installation-steps)
- [🎨 Customization](#-customization)
- [📂 Project Structure](#-project-structure)
- [🔧 Pre-configured Software](#-pre-configured-software)
- [❓ FAQ](#-faq)
- [🤝 Contributing](#-contributing)
- [🌿 Branch Maintenance](#-branch-maintenance)
- [💡 Acknowledgments](#-acknowledgments)
- [📄 License](#-license)

## ✨ Features

🚧 **Project Status: In Development** - We are actively developing new features and improvements

- 🤖 **Deep AI Integration** - Seamlessly integrate large language models into your desktop environment
- 🎨 **Modern UI** - Innovative interface design based on Hyprland and quickshell
- ⚙️ **Flexible Configuration** - Easily customize your workspace using yolk
- 📦 **Pre-configured Optimization** - Out-of-the-box configurations for numerous common software
- 🔄 **Modular Design** - Freely combine your favorite tools through yolk.rhai

## 🎯 Project Goals

PilotSpace aims to create a revolutionary workspace with the following objectives:

- 🧠 **Deep LLM Integration** - Make AI your desktop assistant
- 🎨 **Innovative Interface Design** - Unique, modern, and efficient user experience
- ⚡ **High-Performance Experience** - Based on the Hyprland Wayland compositor
- 🔧 **Intelligent Configuration Management** - Elegant dotfiles management using yolk
- 🌐 **Open Ecosystem** - Support for multiple toolchains and workflows

## 🛠️ Tech Stack

| Component | Technology | Description |
|-----------|------------|-------------|
| 🐚 **Shell** | Zsh | Default shell environment |
| 🪟 **Window Manager** | Hyprland | Modern Wayland compositor |
| 🎛️ **Panel** | quickshell | Flexible desktop components |
| 💻 **Terminal Emulator** | Kitty | GPU-accelerated high-performance terminal |
| ⚙️ **Config Manager** | yolk | Powerful dotfiles management tool |
| 🐍 **Development Language** | Python 3.14+ | Core functionality development |

## 📦 Installation

### System Requirements

- Linux operating system (Arch Linux or derivatives recommended)
- Python 3.14 or higher
- Wayland-compatible display server
- Basic development toolchain

### Installation Steps

This project uses **yolk** to manage configuration files. The installation process is as follows:

#### 1. Install Dependencies

First, ensure all required dependencies are installed:

```bash
# Arch Linux / Manjaro
sudo pacman -S hyprland kitty zsh yolk

# For other distributions, refer to official documentation for each component
```

#### 2. Configure yolk

Bind yolk to the pilotspace-eggs configuration repository:

```bash
# Initialize yolk
yolk init
```

#### 3. Pull and Sync Configuration

```bash
# Pull configuration files
yolk pull

# Sync configuration to system
yolk sync
```

#### 4. Apply Configuration

Log out or restart your system to apply the new desktop environment configuration.

## 🎨 Customization

### How to Preserve Custom Configurations?

PilotSpace is designed as a fully customizable workspace. Recommended customization methods:

1. **Fork This Repository** 🍴
   - Fork the `PilotSpace` repository on GitHub
   - This allows you to keep your modifications and track upstream updates

2. **Modify as Needed** ✏️
   - Edit the `yolk.rhai` file to enable/disable modules
   - Modify configuration files in `PilotSpace-eggs`
   - Adjust themes, keybindings, workflows, etc.

3. **Stay Updated** 🔄
   - Regularly pull updates from the upstream repository
   - Merge new features into your fork

### Configuration File Structure

```
PilotSpace/
├── yolk.rhai              # yolk configuration file
├── PilotSpace-eggs/       # Configuration collection
│   ├── hyprland/         # Hyprland configuration
│   ├── kitty/            # Kitty configuration
│   ├── zsh/              # Zsh configuration
│   └── ...
└── src/                   # Python source code
```

## 📂 Project Structure

### pilotspace-eggs

This is the core subproject for configuration files:

- 📁 **Configuration Collection** - All pre-configured software settings are here
- 🎨 **UI Design Resources** - Themes, icons, wallpapers, and other design assets
- 🔧 **Template Files** - Reusable configuration templates

### pilotspace

Main project repository:

- 📦 **Package Distribution** - Python packages for this project will be published here
- 🤖 **AI Function Modules** - Contains AI-related Python projects
- 🔌 **Plugin System** - Extensions and integration features

## 🔧 Pre-configured Software

This project plans to provide pre-configurations for the following common software:

- ✅ **Shell**: Zsh + Oh My Zsh / Powerlevel10k
- ✅ **Terminal**: Kitty (GPU-accelerated)
- ✅ **Window Manager**: Hyprland (Wayland)
- ✅ **Panel**: quickshell
- 🔄 **Editor**: Neovim (planned)
- 🔄 **File Manager**: Thunar / ranger (planned)
- 🔄 **Browser Config**: Firefox / Chromium (planned)
- 🔄 **Development Tools**: Git, tmux, lazygit (planned)

By editing the `yolk.rhai` file, you can freely choose which pre-configuration combinations to enable.

## ❓ FAQ

### Why Choose yolk?

The author of yolk is also the creator of eww. I discovered this tool while browsing the eww repository, and after trying it out, found it to be excellent:

- ✨ **Advanced Features** - Supports templates, conditional configurations, and more
- 🔄 **Easy Updates** - Simple management and synchronization of configuration files
- 📦 **Modular** - Flexible configuration combination methods
- 🎯 **Built for dotfiles** - Specifically designed, easy to use

**Alternative Tools:**
- [Dotfiles Management Tools Collection](https://dotfiles.github.io/tutorials/)
- GNU Stow
- chezmoi
- yadm

### How to Switch Between Different Combinations?

Installing configuration files is as simple as "hatching eggs":

```bash
# Edit the yolk.rhai file to enable/disable modules
vim yolk.rhai

# Re-sync configuration
yolk sync
```

Simply update the `yolk.rhai` file to easily disable or enable different configuration combinations!

### Which Shells are Supported?

The default is **Zsh**, but we welcome the community to maintain branches for other shells:

- 🐟 **Fish shell** - Maintainers welcome
- 🐚 **Bash** - Maintainers welcome
- ⚡ **Other Zsh frameworks** - Such as prezto, zinit, etc.

## 🤝 Contributing

We warmly welcome all forms of contributions!

### How to Contribute?

1. 🔍 **Submit Issues** - Report bugs or suggest new features
2. 🔧 **Submit Pull Requests** - Directly contribute code or configurations
3. 📝 **Improve Documentation** - Help improve usage instructions
4. 🌐 **Translation** - Help translate documentation into other languages

### Contribution Guidelines

```bash
# 1. Fork this repository
# 2. Create a feature branch
git checkout -b feature/your-feature-name

# 3. Commit your changes
git commit -am "Add some feature"

# 4. Push to the branch
git push origin feature/your-feature-name

# 5. Create a Pull Request
```

Please ensure your code follows project conventions and includes appropriate documentation.

## 🌿 Branch Maintenance

We enthusiastically welcome the community to maintain branches for different configuration solutions!

### Welcome Branch Types

- 🐟 **Fish Shell Version** - Using Fish instead of Zsh
- ⚡ **Different Zsh Frameworks** - Such as prezto, zinit, antigen
- 📝 **Different Neovim Configs** - Such as LunarVim, NvChad, AstroVim
- 🪟 **Other Window Managers** - Such as Sway, i3
- 🎨 **Different Theme Styles** - Dark/light theme variants
- 🖥️ **Desktop Environment Versions** - GNOME/KDE extensions

If you maintain a branch, please let us know through an Issue or PR, and we'll list it in the documentation!

## 💡 Acknowledgments

### Special Thanks

- 🌟 **[end-4/dots-hyprland](https://github.com/end-4/dots-hyprland)** - Thanks to end_4 for excellent Hyprland configuration inspiration
- 🛠️ **[yolk](https://github.com/elkowar/yolk)** - Thanks to elkowar for the powerful configuration management tool
- 🪟 **[Hyprland](https://hyprland.org/)** - Modern Wayland compositor
- 💻 **[Kitty](https://sw.kovidgoyal.net/kitty/)** - Excellent GPU-accelerated terminal

### Community Contributors

Thanks to all developers and users who have contributed to PilotSpace!

## 📄 License

This project is licensed under the **GNU General Public License v3.0**.

For details, please see the [LICENSE](../LICENSE) file.

---

<div align="center">

**Powered by ❤️ and AI**

If this project helps you, please give us a ⭐️ 

[Report Issues](https://github.com/LIghtJUNction/PilotSpace/issues) · [Feature Requests](https://github.com/LIghtJUNction/PilotSpace/issues) · [Discussions](https://github.com/LIghtJUNction/PilotSpace/discussions)

</div>
