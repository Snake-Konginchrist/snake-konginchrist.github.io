# Academic Pages
**Academic Pages 是一个面向个人和专业作品集网站的 GitHub Pages 模板**

![模板示例](images/homepage.png "Academic Pages 模板示例")

# 入门指南

1. 注册 GitHub 账号（若没有）并验证邮箱（必须！）
2. 点击右上角的 "Use this template" 按钮
3. 在新建仓库页面，输入仓库名为 "[你的 GitHub 用户名].github.io"，这将是你的网站地址
4. 配置网站设置并添加内容
5. 上传文件（如 PDF、压缩包等）到 `files/` 目录，可通过 https://[你的 GitHub 用户名].github.io/files/示例.pdf 访问
6. 在仓库设置的 "GitHub Pages" 部分查看状态
7. (可选) 使用 `markdown_generator` 中的 Jupyter notebook 或 Python 脚本从 TSV 文件生成出版物和演讲的 Markdown 文件

更多信息请访问：https://academicpages.github.io/

## 本地运行

在将更改推送到 GitHub 之前，本地预览修改非常有用。本地运行需要以下步骤：

1. 克隆仓库并进行修改
2. 安装 ruby-dev、bundler 和 nodejs

    Linux 和 [WSL](https://learn.microsoft.com/en-us/windows/wsl/about) 系统：
    ```bash
    sudo apt install ruby-dev ruby-bundler nodejs
    ```
    
    MacOS 系统：
    ```bash
    brew install ruby
    brew install node
    gem install bundler
    ```

3. 运行 `bundle install` 安装 Ruby 依赖（若出错可删除 Gemfile.lock 后重试）
4. 运行 `jekyll serve -l -H localhost` 生成 HTML 并通过 `localhost:4000` 访问，服务器会自动重建和刷新页面

Linux 系统可能需要额外依赖：`sudo apt install build-essential gcc make`

### Windows 系统特别说明

推荐使用以下三种方式之一：

1. **Docker 方式（推荐）**
    ```bash
    # 安装 Docker Desktop：https://www.docker.com/products/docker-desktop/
    # 在项目目录打开 PowerShell 执行：
    docker compose up
    ```

2. **WSL 方式（适用于 Windows 10/11）**
    ```bash
    # 1. 启用 WSL 功能（管理员 PowerShell 执行）：
    dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
    # 2. 安装 Ubuntu 发行版：Microsoft Store 搜索安装 Ubuntu
    # 3. 在 WSL 中按 Linux 说明操作即可
    ```

3. **原生 Windows 方式**
    ```bash
    # 1. 安装 Ruby+Devkit：https://rubyinstaller.org/downloads/
    # 2. 安装 Node.js：https://nodejs.org/
    # 3. 安装 MSYS2 开发工具包（Ruby 安装最后一步勾选）：
    ridk install 1 2 3
    # 4. 后续步骤与 Linux/Mac 相同
    ```

注意：原生方式可能需要处理路径问题（建议使用 PowerShell 且项目路径不要包含中文/空格）

**中国大陆用户建议**：
1. 修改 Gemfile 第一行为：`source 'https://mirrors.tuna.tsinghua.edu.cn/rubygems/'`
2. 执行前配置环境变量（PowerShell）：
```bash
$env:RUBYOPT='-ropenssl -rreadline'
```

## 使用 Docker

想要跨平台运行或避免安装依赖？如果已安装 [Docker](https://www.docker.com/)，可以使用提供的 `Dockerfile` 构建容器：

```bash
docker compose up
```

访问 `localhost:4000` 即可查看网站。

# 维护

模板的错误报告和功能请求请通过 [GitHub Issues](https://github.com/academicpages/academicpages.github.io/issues/new/choose) 提交。样式相关问题欢迎在 [GitHub Discussions](https://github.com/academicpages/academicpages.github.io/discussions) 发起讨论。

本仓库从 [Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/) 分支而来（© 2016 Michael Rose，遵循 MIT 许可证）。当前由 [Robert Zupko](https://github.com/rjzupkoii) 维护，欢迎更多维护者加入。

## 错误修复与功能增强

如需提交问题修复或功能增强，请先 [fork 本仓库](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo)（而非使用模板）。这使您可以[同步更新](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/syncing-a-fork)。

注意：由于模板主题的特性，同步核心主题更新时可能会产生冲突。如需保留配置文件和 Markdown 文件，可删除仓库后重新 fork，或手动合并更改。

---
<div align="center">
    
![构建状态](https://github.com/academicpages/academicpages.github.io/actions/workflows/pages/pages-build-deployment/badge.svg)
[![贡献者](https://img.shields.io/github/contributors/academicpages/academicpages.github.io.svg)](https://github.com/academicpages/academicpages.github.io/graphs/contributors)
[![最新版本](https://img.shields.io/github/v/release/academicpages/academicpages.github.io)](https://github.com/academicpages/academicpages.github.io/releases/latest)
[![许可证](https://img.shields.io/github/license/academicpages/academicpages.github.io?color=blue)](https://github.com/academicpages/academicpages.github.io/blob/master/LICENSE)

[![星标数](https://img.shields.io/github/stars/academicpages/academicpages.github.io)](https://github.com/academicpages/academicpages.github.io)
[![复刻数](https://img.shields.io/github/forks/academicpages/academicpages.github.io)](https://github.com/academicpages/academicpages.github.io/fork)
</div>
