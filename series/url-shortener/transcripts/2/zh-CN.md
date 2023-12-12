---
locale: zh-CN
---

## 安装 Choco 和 MySQL

这次视频正好借这个机会，我们来安装一个包管理器，叫做 Choco。Choco 是 Windows 上的包管理器，类似于 Mac 上的 Homebrew。我们可以使用 Choco 来安装我们需要的软件，比如 NodeJS，Git，VSCode 等等。当然，也包含了我们这次需要的 MySQL。

我们可以在 https://chocolatey.org/install 上找到安装 Choco 的方法。我们可以在有管理员权限的 PowerShell 中运行以下命令来安装 Choco：

```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

我们可以在 https://chocolatey.org/packages/mysql 上找到 MySQL 的安装方法。我们可以在有管理员权限的 PowerShell 中运行以下命令来安装 MySQL：

```powershell
choco install mysql
```

## 启动 MySQL

我们可以在 https://dev.mysql.com/doc/refman/8.0/en/windows-start-command-line.html 上找到启动 MySQL 的方法。我们可以在 PowerShell 中运行以下命令来启动 MySQL：

```powershell
mysqld
```

## 连接 MySQL

我们可以在 https://dev.mysql.com/doc/refman/8.0/en/connecting-disconnecting.html 上找到连接 MySQL 的方法。我们可以在 PowerShell 中运行以下命令来连接 MySQL：

```powershell
mysql -u root
```
