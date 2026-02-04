# AzerothCore 通用启动器/ Wotlk PlayerBots 仿官版启动器
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

### v1.0.7.1 (2026-02-04)

#### 🐛 Bug 修复 | Bug Fixes

**修复账号密码长度限制 | Fixed Account Password Length Limit**
- 🇨🇳 放宽用户名和密码长度限制：从最多 5 个字符改为最多 15 个字符
- 🇺🇸 Relaxed username and password length limit: from max 5 characters to max 15 characters
- 🇨🇳 最小长度保持为 1 个字符（不变）
- 🇺🇸 Minimum length remains 1 character (unchanged)

#### 📝 技术细节 | Technical Details

**修改的验证规则 | Modified Validation Rules**
- 🇨🇳 用户名长度：1-5 个字符 → **1-15 个字符**
- 🇺🇸 Username length: 1-5 characters → **1-15 characters**
- 🇨🇳 密码长度：1-5 个字符 → **1-15 个字符**
- 🇺🇸 Password length: 1-5 characters → **1-15 characters**

**影响的功能 | Affected Features**
- 🇨🇳 账号注册：用户名和密码长度限制放宽
- 🇺🇸 Account registration: Username and password length limit relaxed
- 🇨🇳 密码修改：用户名和密码长度限制放宽
- 🇺🇸 Password change: Username and password length limit relaxed

**错误提示更新 | Error Message Updates**
- 🇨🇳 更新中文错误提示："最多5个字符" → "最多15个字符"
- 🇺🇸 Updated Chinese error messages: "max 5 characters" → "max 15 characters"
- 🇨🇳 更新英文错误提示："at most 5 characters" → "at most 15 characters"
- 🇺🇸 Updated English error messages: "at most 5 characters" → "at most 15 characters"

#### 📦 修改的文件 | Modified Files

- `MainWindow.xaml.cs` - 账号注册和密码修改验证逻辑
- `LanguageManager.cs` - 中英文错误提示文本

#### ✅ 验证方法 | Verification Method

**账号注册测试 | Account Registration Test**
- 🇨🇳 尝试注册 1 个字符的用户名和密码（应该成功）
- 🇺🇸 Try registering with 1-character username and password (should succeed)
- 🇨🇳 尝试注册 15 个字符的用户名和密码（应该成功）
- 🇺🇸 Try registering with 15-character username and password (should succeed)
- 🇨🇳 尝试注册 16 个字符的用户名或密码（应该提示"最多15个字符"）
- 🇺🇸 Try registering with 16-character username or password (should show "at most 15 characters" error)

**密码修改测试 | Password Change Test**
- 🇨🇳 尝试修改为 15 个字符的密码（应该成功）
- 🇺🇸 Try changing to 15-character password (should succeed)
- 🇨🇳 尝试修改为 16 个字符的密码（应该提示"最多15个字符"）
- 🇺🇸 Try changing to 16-character password (should show "at most 15 characters" error)

#### ⚠️ 注意事项 | Notes

**数据库兼容性 | Database Compatibility**
- 🇨🇳 AzerothCore 数据库 `account` 表的 `username` 字段类型为 `VARCHAR(32)`
- 🇺🇸 AzerothCore database `account` table `username` field type is `VARCHAR(32)`
- 🇨🇳 修改后的最大长度 15 完全在数据库字段长度范围内
- 🇺🇸 Modified max length 15 is well within database field length limit
- 🇨🇳 不需要修改数据库结构
- 🇺🇸 No database structure modification required

**向后兼容性 | Backward Compatibility**
- 🇨🇳 现有的短用户名和密码（1-5 个字符）仍然有效
- 🇺🇸 Existing short usernames and passwords (1-5 characters) remain valid
- 🇨🇳 不影响已注册的账号
- 🇺🇸 Does not affect already registered accounts
- 🇨🇳 只是放宽了新注册账号的限制
- 🇺🇸 Only relaxes restrictions for new account registrations

---

### v1.0.7.0 (2026-02-03)

#### 🎉 新特性 | New Features

**命令系统全面优化 | Command System Comprehensive Optimization**
- 🇨🇳 397 个控制台命令的完整中文翻译，格式：【中文简述】【语法】【说明】
- 🇺🇸 Complete Chinese translation for 397 console commands, format: [Summary][Syntax][Description]

**智能语言切换 | Intelligent Language Switching**
- 🇨🇳 中文状态显示结构化翻译，英文状态显示原始 help 文本
- 🇺🇸 Chinese mode shows structured translation, English mode shows original help text

**命令列表过滤优化 | Command List Filtering Optimization**
- 🇨🇳 只显示 256 个控制台可用命令（Console::Yes），隐藏不可用命令
- 🇺🇸 Only shows 256 console-available commands (Console::Yes), hides unavailable commands

**BlizzardLike 版本验证 | BlizzardLike Version Validation**
- 🇨🇳 自动检测 worldserver.exe 的 ProductName 属性
- 🇺🇸 Automatically detects worldserver.exe ProductName property
- 🇨🇳 版本不匹配时弹出警告提示
- 🇺🇸 Shows warning when version mismatch detected

#### 🔧 优化改进 | Optimizations

**Updater 更新器重大修复 | Updater Major Fixes**
- 🇨🇳 修复数据库配置读取（支持 `key = value` 格式，正确跳过注释）
- 🇺🇸 Fixed database config reading (supports `key = value` format, correctly skips comments)
- 🇨🇳 MySQL 自动启动功能（路径规范化、输出读取、错误诊断）
- 🇺🇸 MySQL auto-start feature (path normalization, output reading, error diagnosis)
- 🇨🇳 SQL 变量支持（AllowUserVariables=true）
- 🇺🇸 SQL variable support (AllowUserVariables=true)
- 🇨🇳 更新失败重试机制（显示重试按钮，无需重启程序）
- 🇺🇸 Update failure retry mechanism (shows retry button, no restart needed)

**命令翻译质量提升 | Command Translation Quality Improvement**
- 🇨🇳 所有参数占位符已翻译（$account → $账号, $password → $密码等）
- 🇺🇸 All parameter placeholders translated ($account → $账号, $password → $密码, etc.)
- 🇨🇳 关键词智能替换（Create → 创建, Delete → 删除等）
- 🇺🇸 Intelligent keyword replacement (Create → 创建, Delete → 删除, etc.)

#### 🐛 Bug 修复 | Bug Fixes

**修复重复键错误 | Fixed Duplicate Key Error**
- 🇨🇳 删除 `LanguageManager.cs` 中重复的语言资源键
- 🇺🇸 Removed duplicate language resource keys in `LanguageManager.cs`

**修复编译错误 | Fixed Compilation Errors**
- 🇨🇳 修复 `CommandTranslationService.cs` 中的语言检查逻辑（枚举类型比较）
- 🇺🇸 Fixed language check logic in `CommandTranslationService.cs` (enum type comparison)
- 🇨🇳 修复 `ConfigWindow.xaml.cs` 中缺失的 using 引用
- 🇺🇸 Fixed missing using reference in `ConfigWindow.xaml.cs`

**修复 Updater 数据库问题 | Fixed Updater Database Issues**
- 🇨🇳 修复配置键名不匹配（SqlServerIP, ServerPort, SqlServerUser, SqlServerPassword）
- 🇺🇸 Fixed config key name mismatch (SqlServerIP, ServerPort, SqlServerUser, SqlServerPassword)
- 🇨🇳 修复 MySQL 启动路径规范化问题（移除 `\.\` 前缀）
- 🇺🇸 Fixed MySQL startup path normalization issue (removed `\.\` prefix)
- 🇨🇳 修复 SQL 变量支持问题（添加 AllowUserVariables=true）
- 🇺🇸 Fixed SQL variable support issue (added AllowUserVariables=true)

#### 📝 技术细节 | Technical Details

**命令翻译系统 | Command Translation System**
- 🇨🇳 翻译数据来源：数据库 `command` 表（397 个命令）
- 🇺🇸 Translation data source: Database `command` table (397 commands)
- 🇨🇳 翻译生成脚本：`generate_command_translations.py`
- 🇺🇸 Translation generation script: `generate_command_translations.py`
- 🇨🇳 自动更新脚本：`update_command_translations.py`
- 🇺🇸 Auto-update script: `update_command_translations.py`

**版本验证系统 | Version Validation System**
- 🇨🇳 使用 `FileVersionInfo.GetVersionInfo()` 读取 ProductName
- 🇺🇸 Uses `FileVersionInfo.GetVersionInfo()` to read ProductName
- 🇨🇳 验证时机：启动时 + 配置切换时
- 🇺🇸 Validation timing: On startup + On config switch

**Updater 改进 | Updater Improvements**
- 🇨🇳 配置文件支持 `key = value` 格式（带空格）
- 🇺🇸 Config file supports `key = value` format (with spaces)
- 🇨🇳 自动跳过注释行（`#` 开头）
- 🇺🇸 Automatically skips comment lines (starting with `#`)
- 🇨🇳 MySQL 输出实时读取（帮助诊断启动问题）
- 🇺🇸 MySQL output real-time reading (helps diagnose startup issues)
- 🇨🇳 SQL 执行失败时停止更新流程并显示重试按钮
- 🇺🇸 Stops update process and shows retry button when SQL execution fails

#### 📦 修改的文件 | Modified Files

**启动器 | Launcher**:
- `CommandTranslationService.cs` - 集成 397 个命令翻译，修复语言检查逻辑
- `CommandManager.cs` - 命令列表过滤（只显示 Console::Yes 命令）
- `ServerVersionValidator.cs` - 新建，BlizzardLike 版本验证
- `ConfigWindow.xaml.cs` - 添加版本切换验证
- `MainWindow.xaml.cs` - 添加启动时版本验证
- `LanguageManager.cs` - 添加版本验证语言资源

**更新器 | Updater**:
- `AzerothCoreUpdater/Program.cs` - 修复数据库配置读取、MySQL 启动、SQL 变量支持

**脚本 | Scripts**:
- `generate_command_translations.py` - 新建，生成命令翻译
- `update_command_translations.py` - 新建，更新 C# 文件
- `command_translations_generated.cs` - 新建，生成的翻译数据

#### ✅ 验证方法 | Verification Method

**命令翻译验证 | Command Translation Verification**
- 🇨🇳 切换到中文状态，查看命令列表，应显示结构化中文翻译
- 🇺🇸 Switch to Chinese mode, view command list, should show structured Chinese translation
- 🇨🇳 切换到英文状态，查看命令列表，应显示原始英文 help 文本
- 🇺🇸 Switch to English mode, view command list, should show original English help text

**版本验证 | Version Validation**
- 🇨🇳 切换到 BlizzardLike 版本，如果 worldserver.exe 不是仿官版，应弹出警告
- 🇺🇸 Switch to BlizzardLike version, if worldserver.exe is not BlizzardLike, should show warning

**Updater 验证 | Updater Verification**
- 🇨🇳 停止 MySQL，运行更新程序，应自动启动 MySQL 并执行 SQL 更新
- 🇺🇸 Stop MySQL, run updater, should auto-start MySQL and execute SQL updates
- 🇨🇳 如果更新失败，应显示重试按钮，点击重试应重新执行更新流程
- 🇺🇸 If update fails, should show retry button, clicking retry should re-execute update process

---

### v1.0.6.7 (2026-01-31)

#### 🎉 新特性 | New Features

**Worldserver 命令输入功能 | Worldserver Command Input Feature**
- 🇨🇳 启动器新增向 worldserver 发送命令的功能，支持常用命令快捷输入
- 🇺🇸 Added ability to send commands to worldserver from launcher, with quick access to common commands

**命令输入界面 | Command Input Interface**
- 🇨🇳 在世界服务器日志区域添加命令输入框和发送按钮
- 🇺🇸 Added command input box and send button in world server log area

**常用命令下拉菜单 | Common Commands Dropdown**
- 🇨🇳 提供常用命令快捷选择（如 `.server info`, `.help`, `.account create` 等）
- 🇺🇸 Provides quick selection of common commands (e.g., `.server info`, `.help`, `.account create`)

#### 🔧 优化改进 | Optimizations

**完整国际化支持 | Complete Internationalization Support**
- 🇨🇳 修复所有停止服务器日志的硬编码中文问题（16 个新语言资源键）
- 🇺🇸 Fixed all hardcoded Chinese text in server stop logs (16 new language resource keys)

**命令格式优化 | Command Format Optimization**
- 🇨🇳 命令前缀统一为 `AC>`，与 worldserver 控制台保持一致
- 🇺🇸 Unified command prefix to `AC>` to match worldserver console

**日志消息国际化 | Log Message Internationalization**
- 🇨🇳 所有服务器启动、停止、异常日志完全支持中英文切换
- 🇺🇸 All server startup, stop, and exception logs fully support Chinese-English switching

#### 🐛 Bug 修复 | Bug Fixes

**修复重复字典键错误 | Fixed Duplicate Dictionary Key Error**
- 🇨🇳 删除 `LanguageManager.cs` 中重复的 `logWorldServerStopped` 和 `logAuthServerStopped` 键
- 🇺🇸 Removed duplicate `logWorldServerStopped` and `logAuthServerStopped` keys in `LanguageManager.cs`

**修复所有硬编码日志 | Fixed All Hardcoded Logs**
- 🇨🇳 彻底修复停止服务器、启动服务器、程序关闭等所有硬编码中文日志
- 🇺🇸 Completely fixed all hardcoded Chinese logs for server stop, start, and program closing

#### 🔧 配套服务器更新 | Bundled Server Updates

**Worldserver 控制台命令修复 | Worldserver Console Command Fix**
- 🇨🇳 修复 worldserver.exe 控制台命令输出不显示的问题
- 🇺🇸 Fixed worldserver.exe console command output not displaying issue

**问题根源 | Root Cause**
- 🇨🇳 `utf8print` 函数在 Windows 平台缺少 `fflush(stdout)`，导致命令输出被缓冲
- 🇺🇸 `utf8print` function missing `fflush(stdout)` on Windows platform, causing command output to be buffered

**诊断日志系统 | Diagnostic Logging System**
- 🇨🇳 添加完整的 CLI 线程诊断日志（启动、命令接收、排队、EOF 检测等）
- 🇺🇸 Added comprehensive CLI thread diagnostic logging (startup, command reception, queuing, EOF detection, etc.)

#### 📝 技术细节 | Technical Details

**启动器修改 | Launcher Modifications**
- 🇨🇳 新增语言资源（16 个）| 🇺🇸 New Language Resources (16 total):
  - **停止服务器日志 | Server Stop Logs (8)**:
    - `logStoppingWorldServer` - 正在停止世界服务器 | Stopping world server
    - `logWorldServerStopped` - 世界服务器已停止 | World server stopped
    - `logWorldServerStopException` - 世界服务器停止异常 | World server stop exception
    - `logStoppingAuthServer` - 正在停止认证服务器 | Stopping auth server
    - `logAuthServerStopped` - 认证服务器已停止 | Auth server stopped
    - `logAuthServerStopException` - 认证服务器停止异常 | Auth server stop exception
    - `logStoppingMySQLProcesses` - 正在停止 MySQL 进程 | Stopping MySQL processes
    - `logAllServersStopped` - 所有服务器已停止 | All servers stopped
  
  - **启动服务器日志 | Server Start Logs (5)**:
    - `logAuthServerStarted2` - 认证服务器已启动 | Auth server started
    - `logAuthServerStartFailed` - 认证服务器启动失败 | Auth server start failed
    - `logAuthServerStartException` - 认证服务器启动异常 | Auth server start exception
    - `logWorldServerStartFailed` - 世界服务器启动失败 | World server start failed
    - `logWorldServerStartException` - 世界服务器启动异常 | World server start exception
  
  - **其他日志 | Other Logs (3)**:
    - `logProgramClosing` - 程序关闭消息 | Program closing message
    - `logFoundOldUpdater` - 发现旧更新程序 | Found old updater
    - `msgCommandSent` - 命令发送消息 | Command sent message

**服务器端修改 | Server-Side Modifications**
- `1.SourceCode/src/server/apps/worldserver/CommandLine/CliRunnable.cpp`
  - 修复 `utf8print` 函数缺少 `fflush(stdout)` 的问题
  - 添加 CLI 线程诊断日志系统
  - 添加 stdin 有效性检查（Windows 平台）

- `1.SourceCode/src/server/apps/worldserver/Main.cpp`
  - 添加 CLI 线程创建日志
  - 添加控制台禁用原因日志

**代码标记 | Code Markers**
- 🇨🇳 所有修改使用 `//by leewheel 20260131` 和 `//end leewheel` 标记
- 🇺🇸 All modifications marked with `//by leewheel 20260131` and `//end leewheel`

#### 📦 修改的文件 | Modified Files

**启动器 | Launcher**:
- `LanguageManager.cs` - 添加 16 个新语言资源键，删除重复键
- `MainWindow.xaml.cs` - 更新所有硬编码日志为国际化调用，添加命令输入功能
- `MainWindow.xaml` - 添加命令输入界面元素

**服务器 | Server**:
- `1.SourceCode/src/server/apps/worldserver/CommandLine/CliRunnable.cpp`
- `1.SourceCode/src/server/apps/worldserver/Main.cpp`

#### ✅ 验证方法 | Verification Method

**启动器命令输入 | Launcher Command Input**
- 🇨🇳 在启动器的世界服务器日志区域输入命令（如 `.server info`），点击发送按钮
- 🇺🇸 Enter command in launcher's world server log area (e.g., `.server info`), click send button

**控制台命令输出 | Console Command Output**
- 🇨🇳 在 worldserver.exe 控制台直接输入命令，应立即看到输出
- 🇺🇸 Enter command directly in worldserver.exe console, output should appear immediately

---

### v1.0.6.6 (2026-01-31)

#### 🎉 新特性 | New Features

**服务器自动重启功能 | Server Auto-Restart Feature**
- 🇨🇳 服务器崩溃时自动重启，带10秒倒计时显示
- 🇺🇸 Automatic server restart on crash with 10-second countdown display

**重启倒计时国际化 | Restart Countdown Internationalization**
- 🇨🇳 重启倒计时消息完整支持中英文切换
- 🇺🇸 Restart countdown messages fully support Chinese-English switching

**重启指示灯闪烁效果 | Restart Indicator Flashing Effect**
- 🇨🇳 重启倒计时期间指示灯橙色/红色交替闪烁
- 🇺🇸 Indicator alternates between orange and red during restart countdown

**自动重启开关 | Auto-Restart Toggle**
- 🇨🇳 可通过"崩溃自动重启"复选框启用/禁用自动重启功能
- 🇺🇸 Enable/disable auto-restart via "Auto-Restart on Crash" checkbox

#### 🔧 优化改进 | Optimizations

**完整国际化支持 | Complete Internationalization Support**
- 🇨🇳 添加 22 个新的语言资源键，覆盖所有服务器启动、停止、异常日志
- 🇺🇸 Added 22 new language resource keys covering all server startup, stop, and exception logs

**服务器命令格式优化 | Server Command Format Optimization**
- 🇨🇳 命令前缀从 `>>>` 改为 `AC>`，更符合 AzerothCore 风格
- 🇺🇸 Command prefix changed from `>>>` to `AC>` for better AzerothCore style

**下拉菜单深色主题 | Dropdown Menu Dark Theme**
- 🇨🇳 常用命令下拉菜单背景色改为深色（#050A14），更统一美观
- 🇺🇸 Common commands dropdown menu background changed to dark color (#050A14) for better consistency

**改进日志消息 | Improved Log Messages**
- 🇨🇳 优化重启倒计时消息格式，使用 `string.Format()` 支持参数化
- 🇺🇸 Optimized restart countdown message format using `string.Format()` for parameterization

**视觉效果优化 | Visual Effect Optimization**
- 🇨🇳 重启倒计时期间指示灯闪烁更加明显和流畅
- 🇺🇸 More prominent and smooth indicator flashing during restart countdown

#### 🐛 Bug 修复 | Bug Fixes

**修复单文件发布错误 | Fixed Single File Publishing Error**
- 🇨🇳 修复 "Unknown hard error" 错误：添加编码提供程序异常保护
- 🇺🇸 Fixed "Unknown hard error": Added encoding provider exception protection

**修复重复字典键 | Fixed Duplicate Dictionary Key**
- 🇨🇳 删除 `LanguageManager.cs` 中重复的 `msgPasswordChangeFailed` 键
- 🇺🇸 Removed duplicate `msgPasswordChangeFailed` key in `LanguageManager.cs`

**修复所有硬编码中文字符串 | Fixed All Hardcoded Chinese Strings**
- 🇨🇳 彻底修复所有服务器启动、停止、异常日志的硬编码中文问题
- 🇺🇸 Completely fixed all hardcoded Chinese text in server startup, stop, and exception logs

**修复自动重启消息无国际化 | Fixed Auto-Restart Messages Without Internationalization**
- 🇨🇳 修复崩溃和重启倒计时消息硬编码中文的问题
- 🇺🇸 Fixed hardcoded Chinese text in crash and restart countdown messages

**修复消息格式化问题 | Fixed Message Formatting Issues**
- 🇨🇳 修复重启消息参数顺序和格式化问题
- 🇺🇸 Fixed parameter order and formatting issues in restart messages

#### 📝 技术细节 | Technical Details
- 🇨🇳 新增语言资源（共 22 个）| 🇺🇸 New Language Resources (22 total):
  - **自动重启相关 | Auto-Restart Related (6)**:
    - `logAuthServerCrashed` - 认证服务器崩溃消息 | Auth server crash message
    - `logWorldServerCrashed` - 世界服务器崩溃消息 | World server crash message
    - `logRestartingIn` - 重启倒计时开始消息 | Restart countdown start message
    - `logRestartCountdown` - 重启倒计时消息 | Restart countdown message
    - `logAuthServerName` - 认证服务器名称 | Auth server name
    - `logWorldServerName` - 世界服务器名称 | World server name
  
  - **停止服务器相关 | Server Stop Related (8)**:
    - `logStoppingWorldServer` - 正在停止世界服务器 | Stopping world server
    - `logWorldServerStopped` - 世界服务器已停止 | World server stopped
    - `logWorldServerStopException` - 世界服务器停止异常 | World server stop exception
    - `logStoppingAuthServer` - 正在停止认证服务器 | Stopping auth server
    - `logAuthServerStopped` - 认证服务器已停止 | Auth server stopped
    - `logAuthServerStopException` - 认证服务器停止异常 | Auth server stop exception
    - `logStoppingMySQLProcesses` - 正在停止 MySQL 进程 | Stopping MySQL processes
    - `logAllServersStopped` - 所有服务器已停止 | All servers stopped
  
  - **启动服务器相关 | Server Start Related (5)**:
    - `logAuthServerStarted2` - 认证服务器已启动 | Auth server started
    - `logAuthServerStartFailed` - 认证服务器启动失败 | Auth server start failed
    - `logAuthServerStartException` - 认证服务器启动异常 | Auth server start exception
    - `logWorldServerStartFailed` - 世界服务器启动失败 | World server start failed
    - `logWorldServerStartException` - 世界服务器启动异常 | World server start exception
  
  - **其他日志 | Other Logs (3)**:
    - `logProgramClosing` - 程序关闭消息 | Program closing message
    - `logFoundOldUpdater` - 发现旧更新程序 | Found old updater
    - `msgCommandSent` - 命令发送消息 | Command sent message

#### 📦 修改的文件 | Modified Files
- `App.xaml.cs` - 添加编码提供程序异常保护
- `LanguageManager.cs` - 添加 22 个新的语言资源键，删除重复键
- `MainWindow.xaml.cs` - 更新所有硬编码消息为国际化调用
- `MainWindow.xaml` - 更新下拉菜单背景色

---

### v1.0.6.4 (2026-01-30)

#### 🎉 新特性 | New Features

**单文件大幅瘦身 | Single File Size Optimization**
- 🇨🇳 通过组合优化方案（GZip 压缩 + ReadyToRun + 移除调试符号），主程序从 80 MB 降至 45-55 MB，减少约 35-45%
- 🇺🇸 Reduced main program size from 80 MB to 45-55 MB (35-45% reduction) through combined optimization (GZip compression + ReadyToRun + debug symbols removal)

**下载失败重试功能 | Download Retry Feature**
- 🇨🇳 Updater 下载窗口新增重试按钮，下载失败后可一键重试，无需重启程序
- 🇺🇸 Added retry button in Updater download window, allowing one-click retry after download failure without restarting

**错误信息多行显示 | Multi-line Error Display**
- 🇨🇳 错误提示改为多行显示控件，支持自动换行和滚动，长错误信息更清晰易读
- 🇺🇸 Error messages now displayed in multi-line control with auto-wrap and scrolling for better readability

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

**UI 改进 | UI Improvements**
- 🇨🇳 机器人配置按钮图标从 👤 改为 🤖，更直观易识别
- 🇺🇸 Bot configuration button icon changed from 👤 to 🤖 for better recognition

- 🇨🇳 所有顶部按钮增加间距（5px），布局更舒适
- 🇺🇸 Added spacing (5px) between all top buttons for better layout

- 🇨🇳 优化 ToolTip 显示时长，鼠标离开后立即消失
- 🇺🇸 Optimized ToolTip display duration, disappears immediately when mouse leaves

- 🇨🇳 修复英文状态下主标题显示不全的问题
- 🇺🇸 Fixed main title truncation issue in English mode

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
