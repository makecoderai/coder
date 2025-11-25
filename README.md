# coder - 超级编程智能体

## 介绍

[Coder](https://makecoder.com/) 是一个超级编程智能体，零配置，使用`多模型 x 多智能体`，内置Claude Code、Codex CLI、Gemini CLI多智能体引擎调度，可以切换Claude、GPT、Gemini、Deepseek、Kimi、GLM等领先模型。

[MakeCoder 免费注册&领取积分](https://makecoder.com/)

## 安装

### 前置环境

#### Node.js

Coder 依赖于 Node.js 包管理器 **npm**。请根据您的操作系统安装对应的 Node.js 环境（版本推荐 v18+）。

| **操作系统** | **安装方法** |
|----|----|
| **macOS** | 推荐使用 **Homebrew**：brew install node |
| **Linux** | 推荐使用发行版包管理器，例如 **apt**：sudo apt install nodejs npm，或使用 **nvm** (Node Version Manager) |
| **Windows** | 访问 [Node.js 官网](https://nodejs.org/) 下载并安装（安装程序默认会包含 npm） |

AI解答：<https://makecoder.com/chat/share/0aeb363f-334e-4fc9-b59c-c70d5003d371>

#### git bash

* 只 Windows 需要
* PowerShell > `winget install --id Git.Git -e`
* AI解答：<https://makecoder.com/chat/share/d2955b52-3da4-4ece-b71c-c0bccc3747d5>

💡 **提示**：后续在 Windows 上使用 Coder 时，建议始终在 Git Bash 终端中运行命令，例如 coder、npm 等，以避免因命令语法差异导致的问题。

### Coder安装

* 通过 npm 从 Makecoder 提供的 tarball 文件进行安装

  ```python
  npm install -g https://makecoder.com/download/makecoder-coder-latest
  ```
* 运行 `coder --version` 查看安装的版本号
* ⚠️ **注意**:
  * `-g` 标志表示全局安装，使您可以在任何目录下运行 `coder` 命令。
  * `-latest` 表示安装最新版本，安装特定版本示例 `makecoder-coder-1.0.6.tgz`
  * 官方提供的下载地址和版本号应以 MakeCoder 平台的最新信息为准。

### Coder 用户认证

* 登录 MakeCoder，创建和复制 [API Key](https://makecoder.com/my/apikeys)
* 在电脑终端上运行以下命令为Coder配置API Key

  ```python
  coder --save-auth --aksk <平台复制的 apikey>
  ```

  ✅ **成功提示**: 配置成功后，终端会显示：✅ 认证信息已保存到配置文件。

## 使用

### 交互模型运行

在命令行终端输入 `coder` 开始AI编程

```python
# 开始 coder AI编程
coder

# 也可以在命令行中输入任务
coder "使用 Python 编写一个快速排序算法并输出到 sort.py 文件"

# -p 执行完成后退出
coder "使用 Python 编写一个快速排序算法并输出到 sort.py 文件"
```


### 切换模型

```python
/model

 Select model
 Switch between models. Applies to this session and future sessions. For custom model names, specify with --model.

 ❯ 1.  Claude Sonnet 4.5   Use the default model Claude Sonnet 4.5 · 1.5x/1.88x per Mtok
   2.  Claude Haiku 4.5    Claude Haiku 4.5 模型。0.53x~
   3.  GPT-5               GPT-5 for complex tasks · 1x/1x per Mtok
   4.  GPT-5.1             GPT-5 for complex tasks · 1x/1x per Mtok
   5.  GPT o3              GPT o3 for complex tasks · 1x/1x per Mtok
   6.  Claude Opus 4.5     Claude Opus 4.1 for complex tasks · 2.5x/3.12x per Mtok ✔
   7.  Gemini 2.5 Flash    Gemini 2.5 Flash for complex tasks · 0.15x/0.32x per Mtok
   8.  Gemini 2.5 Pro      Gemini 2.5 Pro for complex tasks · 1x/1x per Mtok
   9.  DeepSeek-V3.1       DeepSeek-V3.1 for complex tasks · 0.14x/0.17x per Mtok
   10. DeepSeek-R1         DeepSeek-R1 for complex tasks · 0.29x/0.29x per Mtok
   11. Qwen Max            Qwen Max for complex tasks · 0.17x/0.17x per Mtok
   12. Qwen3 Coder Plus    Qwen3 Coder Plus for complex tasks · 0.29x/0.29x per Mtok
   13. Kimi K2             Kimi-K2 for complex tasks · 0.29x/0.29x per Mtok
   14. Doubao Seed 1.6     DoubanSeed-1.6 for complex tasks · 0.06x/0.04x per Mtok
   15. GLM 4.5             GLM-4.5 for complex tasks · 0.29x/0.29x per Mtok

```

### 调用特定智能体

```python
coder claude
coder codex
coder gemini
```

## FAQ

* Q：在 Windows 上运行 Coder codex 时出现 Child process exited with code: 3221225781 怎么办？

  A：这通常是由于缺少必需的 C++ 运行库。请下载并安装 [Visual C++ Redistributable for Visual Studio 2015-2022（64 位）](https://aka.ms/vs/17/release/vc_redist.x64.exe)，安装完成后重新打开 Git Bash 并再次运行 coder codex。
* 更多问题\nASK AI：<https://makecoder.com/>


