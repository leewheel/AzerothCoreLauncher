# AzerothCore 通用启动器
# AzerothCore General Launcher

## 项目简介 | Project Introduction

AzerothCore 通用启动器是一个基于 WPF 开发的图形化工具，用于简化 AzerothCore 服务器的启动、管理和配置。它提供了直观的用户界面，支持中英文双语切换，帮助用户轻松管理 AzerothCore 服务器。

AzerothCore General Launcher is a graphical tool developed based on WPF, designed to simplify the startup, management, and configuration of AzerothCore servers. It provides an intuitive user interface with support for Chinese-English bilingual switching, helping users easily manage their AzerothCore servers.

## 功能特性 | Features

### 核心功能 | Core Features
- ✅ **服务器控制**：一键启动/停止认证服务器和世界服务器
- ✅ **账号管理**：注册账号、修改密码、账号管理功能
- ✅ **配置管理**：可视化配置数据库连接和客户端路径
- ✅ **日志监控**：实时查看认证服务器和世界服务器日志
- ✅ **状态监控**：直观显示服务器运行状态
- ✅ **客户端启动**：一键启动魔兽世界客户端

### 高级功能 | Advanced Features
- 🌐 **中英文双语支持**：一键切换界面语言
- 🎨 **科幻风格界面**：现代化的用户界面设计
- 🔄 **自动配置**：自动生成和管理配置文件
- ⚙️ **MySQL 管理**：自动检查和启动 MySQL 服务
- 📊 **实时日志**：实时监控服务器日志输出
- 🎵 **动态效果**：带有动画效果的用户界面

## 系统要求 | System Requirements

- **操作系统**：Windows 10/11 64位
- **.NET 版本**：.NET 10.0 或更高版本
- **内存**：至少 4GB RAM
- **磁盘空间**：至少 1GB 可用空间
- **AzerothCore**：已编译的 AzerothCore 服务器文件
- **MySQL**：MySQL 8.0 或更高版本

## 快速开始 | Quick Start

1. **下载启动器**：从 GitHub Releases 下载最新版本的启动器
2. **解压文件**：将下载的压缩包解压到任意目录
3. **准备服务器文件**：将已编译的 AzerothCore 服务器文件（authserver.exe、worldserver.exe）放在启动器同一目录下
4. **运行启动器**：双击 `AzerothCoreGeneralLauncher.exe` 运行启动器
5. **配置设置**：点击齿轮图标进入配置界面，设置数据库连接和客户端路径
6. **启动服务器**：点击"启动服务器"按钮启动认证服务器和世界服务器
7. **启动客户端**：服务器启动成功后，点击"启动客户端"按钮启动游戏

## 安装与使用 | Installation & Usage

### 安装 | Installation

1. 确保你的系统已安装 .NET 10.0 或更高版本
2. 从 GitHub Releases 下载最新版本的启动器
3. 将下载的 `AzerothCoreGeneralLauncher.zip` 解压到任意目录
4. 将已编译的 AzerothCore 服务器文件（authserver.exe、worldserver.exe）复制到启动器目录
5. 确保 MySQL 服务已正确安装和配置

### 使用说明 | Usage Instructions

#### 首次使用 | First-time Use

1. 运行 `AzerothCoreGeneralLauncher.exe`
2. 系统会自动创建 `configs` 目录和默认配置文件
3. 点击右上角的齿轮图标进入配置界面
4. 设置数据库连接参数：
   - 数据库IP：默认为 127.0.0.1
   - 服务器端口：默认为 3306
   - 数据库用户名：默认为 acore
   - 数据库密码：默认为 acore
5. 设置客户端路径：
   - 点击浏览按钮选择你的魔兽世界客户端目录中的 wow.exe 文件
6. 点击"保存并关闭"按钮保存配置

#### 启动服务器 | Starting the Server

1. 确保 MySQL 服务已运行
2. 点击"启动服务器"按钮
3. 等待启动器完成以下步骤：
   - 清理现有的 MySQL 进程
   - 启动 MySQL 服务（如果未运行）
   - 启动认证服务器
   - 启动世界服务器
4. 当所有服务器状态指示灯变为绿色时，表示服务器已成功启动
5. 点击"启动客户端"按钮启动游戏客户端

#### 停止服务器 | Stopping the Server

1. 点击"停止服务器"按钮
2. 启动器会自动停止世界服务器、认证服务器和 MySQL 服务
3. 等待所有服务器状态指示灯变为红色，表示服务器已成功停止

## 配置说明 | Configuration

### 配置文件 | Configuration Files

启动器的配置文件位于 `configs` 目录下：

- `AzerothCoreLauncher.config`：主配置文件，包含数据库连接和客户端路径设置
- `language.config`：语言偏好设置文件

### 配置项说明 | Configuration Options

#### 主配置文件 | Main Configuration File

```ini
# 客户端路径配置
# Client Path Configuration
client = D:\WoWClient\World of Warcraft 3.3.5a.12340 zhCN\wow.exe

# 数据库连接配置
# Database Connection Configuration
SqlServerIP = 127.0.0.1
ServerPort = 3306
SqlServerUser = acore
SqlServerPassword = acore
```

#### 语言配置 | Language Configuration

语言配置文件 `language.config` 包含当前使用的语言设置：

- `Chinese`：中文
- `English`：英文

## 常见问题 | FAQ

### Q: 启动器无法找到服务器文件怎么办？
A: 请确保将已编译的 AzerothCore 服务器文件（authserver.exe、worldserver.exe）放在启动器同一目录下。

### Q: 数据库连接失败怎么办？
A: 请检查：
1. MySQL 服务是否已启动
2. 数据库IP、端口、用户名和密码是否正确
3. 数据库用户是否有足够的权限

### Q: 如何切换界面语言？
A: 点击右上角的语言按钮（CN/EN）即可切换界面语言。

### Q: 启动客户端失败怎么办？
A: 请检查：
1. 客户端路径是否正确设置
2. wow.exe 文件是否存在
3. 魔兽世界客户端版本是否为 3.3.5a

## 技术支持 | Technical Support

### 联系方式 | Contact Information
- **作者**：leewheel
- **GitHub**：[https://github.com/leewheel/AzerothCoreLauncher](https://github.com/leewheel/AzerothCoreLauncher)
- **Discord**：[AzerothCore Discord](https://discord.gg/azerothcore)

### 提交问题 | Submit Issues

如果您在使用过程中遇到问题，请在 GitHub Issues 中提交详细的问题描述，包括：

1. 操作系统版本
2. .NET 版本
3. 启动器版本
4. 详细的错误信息
5. 问题重现步骤

## 贡献指南 | Contributing

欢迎所有形式的贡献，包括：

- 报告 bug
- 提出新功能建议
- 提交代码修复
- 改进文档
- 翻译界面

### 开发环境搭建 | Development Environment Setup

1. 安装 Visual Studio 2025 或更高版本
2. 克隆项目仓库
3. 打开 `AzerothCoreBlizzardLike2026.csproj` 项目
4. 还原 NuGet 依赖
5. 编译并运行项目

## 许可证 | License

本项目采用 MIT 许可证，详情请查看 [LICENSE](LICENSE) 文件。

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 更新日志 | Changelog

### v1.0.0 (2026-01-26)

- ✨ 初始版本发布
- ✅ 实现服务器控制功能
- ✅ 实现账号管理功能
- ✅ 实现配置管理功能
- ✅ 实现日志监控功能
- ✅ 实现中英文双语支持
- ✅ 实现科幻风格界面

## 致谢 | Acknowledgments

- [AzerothCore](https://azerothcore.org/)：提供了优秀的魔兽世界服务器框架
- [WPF](https://learn.microsoft.com/en-us/dotnet/desktop/wpf/)：提供了强大的桌面应用开发框架
- [MySQL](https://www.mysql.com/)：提供了可靠的数据库服务
- [NAudio](https://github.com/naudio/NAudio)：提供了音频处理支持
- [AvalonEdit](https://github.com/icsharpcode/AvalonEdit)：提供了代码编辑控件支持

## 免责声明 | Disclaimer

本项目仅用于学习和研究目的，不得用于商业用途。使用本项目时，请遵守相关法律法规和游戏版权协议。

This project is for learning and research purposes only and shall not be used for commercial purposes. When using this project, please comply with relevant laws, regulations, and game copyright agreements.

---

**享受使用 AzerothCore 通用启动器！**
**Enjoy using AzerothCore General Launcher!**

---

© 2026 leewheel. All rights reserved.