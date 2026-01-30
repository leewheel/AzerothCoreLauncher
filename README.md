# AzerothCore 通用启动器
# AzerothCore General Launcher
## Since it integrates the.NET 10 environment and all updates, the single file is relatively large.

<img width="2204" height="1706" alt="image" src="https://github.com/user-attachments/assets/5162cba3-3396-4f8c-bdd9-62095398a275" />
<img width="2194" height="1700" alt="image" src="https://github.com/user-attachments/assets/39591bc5-0aae-448c-8d8d-c90fb4b5eee8" />
<img width="2198" height="1718" alt="image" src="https://github.com/user-attachments/assets/66599669-6b9a-4bf0-bf3c-6abad60460e2" />
<img width="2198" height="1706" alt="image" src="https://github.com/user-attachments/assets/ca9ae9e6-dcf5-461e-920b-4a776f0e6be3" />
<img width="2212" height="1716" alt="image" src="https://github.com/user-attachments/assets/a55a45c9-48ca-4d37-be31-133ff1c1822c" />





## 项目简介 | Project Introduction

AzerothCore 通用启动器是一个基于 WPF 开发的图形化工具，用于简化 AzerothCore 服务器的启动、管理和配置。它提供了直观的用户界面，支持中英文双语切换，帮助用户轻松管理 AzerothCore 服务器。

AzerothCore General Launcher is a graphical tool developed based on WPF, designed to simplify the startup, management, and configuration of AzerothCore servers. It provides an intuitive user interface with support for Chinese-English bilingual switching, helping users easily manage their AzerothCore servers.

---

## 更新日志 | Changelog

### v1.0.5 (2026-01-30)

#### 🎉 新特性 | New Features

**单文件大幅瘦身 | Single File Size Optimization**
- 🇨🇳 通过组合优化方案（GZip 压缩 + ReadyToRun + 移除调试符号），主程序从 80 MB 降至 45-55 MB，减少约 35-45%
- 🇺🇸 Reduced main program size from 80 MB to 45-55 MB (35-45% reduction) through combined optimization (GZip compression + ReadyToRun + debug symbols removal)

#### 🔧 优化改进 | Optimizations

**启用 ReadyToRun 编译 | Enabled ReadyToRun Compilation**
- 🇨🇳 AOT 预编译提升启动速度和运行性能
- 🇺🇸 AOT pre-compilation improves startup speed and runtime performance

**GZip 压缩嵌入资源 | GZip Compressed Embedded Resources**
- 🇨🇳 Updater.exe 压缩后嵌入主程序，压缩率约 30-40%
- 🇺🇸 Updater.exe compressed before embedding, achieving 30-40% compression ratio

**移除调试符号 | Removed Debug Symbols**
- 🇨🇳 Release 版本不再包含调试信息，进一步减小文件大小
- 🇺🇸 Release builds no longer include debug information for smaller file size

**启用单文件内部压缩 | Enabled Single File Compression**
- 🇨🇳 .NET 运行时和依赖库自动压缩
- 🇺🇸 .NET runtime and dependencies automatically compressed

#### 📝 技术细节 | Technical Details
- 🇨🇳 编译器优化 | 🇺🇸 Compiler Optimization: `Optimize=true`
- 🇨🇳 分层编译 | 🇺🇸 Tiered Compilation: `TieredCompilation=true`
- 🇨🇳 预编译 | 🇺🇸 ReadyToRun: `PublishReadyToRun=true`
- 🇨🇳 单文件压缩 | 🇺🇸 Single File Compression: `EnableCompressionInSingleFile=true`
- 🇨🇳 调试符号 | 🇺🇸 Debug Symbols: `DebugType=none`, `DebugSymbols=false`

#### 📦 文件大小对比 | File Size Comparison
- **🇨🇳 主程序 | 🇺🇸 Main Program**: 80 MB → 45-55 MB (-35~45%)
- **Updater.exe**: 65 MB → 55-60 MB (🇨🇳 优化后 | 🇺🇸 optimized)
- **Updater.exe.gz**: 35-40 MB (🇨🇳 压缩后 | 🇺🇸 compressed)

#### ⚠️ 注意事项 | Notes

**解压时间 | Decompression Time**
- 🇨🇳 首次释放 Updater.exe 时增加约 0.5-1 秒解压时间（用户无感知）
- 🇺🇸 First-time Updater.exe extraction adds ~0.5-1 second decompression time (imperceptible to users)

**向后兼容 | Backward Compatibility**
- 🇨🇳 保持向后兼容：如果没有压缩版本，仍可使用未压缩的 Updater.exe
- 🇺🇸 Backward compatible: Falls back to uncompressed Updater.exe if compressed version unavailable

---

### v1.0.4 (2026-01-29)

#### 🎉 新特性 | New Features

**全新更新流程 | New Update Workflow**
- 🇨🇳 程序启动时自动后台检查更新，发现新版本立即释放 Updater.exe 并显示更新按钮呼吸灯效果
- 🇺🇸 Automatic background update check on startup, immediate Updater.exe extraction and breathing light effect on update button when new version found

**漂亮的下载窗口 | Beautiful Download Window**
- 🇨🇳 青色发光边框 UI，实时显示下载进度、速度和剩余时间
- 🇺🇸 Cyan glowing border UI with real-time download progress, speed, and remaining time

**中英文双语完整支持 | Complete Bilingual Support**
- 🇨🇳 主程序和 Updater.exe 完全支持中英文切换，通过 `configs/language.config` 自动同步
- 🇺🇸 Main program and Updater.exe fully support Chinese-English switching, automatically synced via `configs/language.config`

#### 🔧 优化改进 | Optimizations

**主窗口标题居中 | Centered Main Window Title**
- 🇨🇳 tbMainTitle 控件文字居中显示
- 🇺🇸 tbMainTitle control text centered

**Updater 按钮居中 | Centered Updater Buttons**
- 🇨🇳 下载窗口的取消按钮居中显示，重试按钮失败时显示在右侧
- 🇺🇸 Cancel button centered in download window, retry button appears on right when failed

**自动清理 Updater.exe | Auto Cleanup Updater.exe**
- 🇨🇳 主程序启动时自动删除旧的隐藏 Updater.exe
- 🇺🇸 Main program automatically deletes old hidden Updater.exe on startup

**版本号显示优化 | Version Display Optimization**
- 🇨🇳 更新按钮提示显示 `v1.0.4 → 1.0.5` 格式
- 🇺🇸 Update button tooltip shows `v1.0.4 → 1.0.5` format

#### 🐛 Bug 修复 | Bug Fixes

**修复底部版本号被裁剪 | Fixed Bottom Version Number Clipping**
- 🇨🇳 移除负边距，增加 MinHeight 到 45
- 🇺🇸 Removed negative margin, increased MinHeight to 45

**修复 Updater.exe 单文件发布 | Fixed Updater.exe Single File Publishing**
- 🇨🇳 使用 `dotnet publish` 生成 65 MB 单文件
- 🇺🇸 Using `dotnet publish` to generate 65 MB single file

#### 📝 技术细节 | Technical Details
- 🇨🇳 Updater.exe 从 WindowsForms 改为 WPF | 🇺🇸 Updater.exe migrated from WindowsForms to WPF
- 🇨🇳 添加应用程序图标（app.ico）| 🇺🇸 Added application icon (app.ico)
- 🇨🇳 新增 `UpdaterLanguageManager.cs` 支持双语 | 🇺🇸 Added `UpdaterLanguageManager.cs` for bilingual support
- 🇨🇳 主程序 `UpdateManager.cs` 重构为新流程 | 🇺🇸 Main program `UpdateManager.cs` refactored for new workflow
- 🇨🇳 Updater 负责关闭主程序并完成更新 | 🇺🇸 Updater handles closing main program and completing update

---

© 2026 leewheel. All rights reserved.
