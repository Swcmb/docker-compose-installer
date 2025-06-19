
# 🐳 Docker Compose Installers Sync

本项目通过 GitHub Actions 自动每日同步并发布 Docker Compose 各平台安装包，方便在国内或受限网络环境中获取官方安装器。

## 📦 已同步安装包

每天自动发布以下平台的 Docker Compose 安装包至 GitHub Releases：

### ✅ Linux

- `x86_64`
- `aarch64`（ARM64）
- `armv6`
- `armv7`
- `ppc64le`
- `riscv64`
- `s390x`

### 🍎 macOS

- `x86_64`（Intel）
- `aarch64`（Apple Silicon）

### 🪟 Windows

- `x86_64`
- `aarch64`

## 🔄 自动同步机制

- 每天 00:00 UTC 自动同步最新官方版本（使用 GitHub Actions）
- 可手动点击 GitHub 的 [Actions 页面](https://github.com/Swcmb/docker-compose-installer/actions) 触发同步
- 安装包文件发布在 [Releases 页面](https://github.com/Swcmb/docker-compose-installer/releases)

## 🛠️ 如何安装

选择对应系统架构，从 Releases 页面下载你需要的版本并赋予可执行权限（Linux/macOS）：

### Linux 示例：

```bash
curl -LO https://github.com/Swcmb/docker-compose-installer/releases/latest/download/docker-compose-linux-x86_64
chmod +x docker-compose-linux-x86_64
sudo mv docker-compose-linux-x86_64 /usr/local/bin/docker-compose
docker-compose version
```

### macOS 示例：

```bash
curl -LO https://github.com/Swcmb/docker-compose-installer/releases/latest/download/docker-compose-darwin-aarch64
chmod +x docker-compose-darwin-aarch64
sudo mv docker-compose-darwin-aarch64 /usr/local/bin/docker-compose
docker-compose version
```

### Windows 示例：

从浏览器打开 [Releases 页面](https://github.com/Swcmb/docker-compose-installer/releases)，下载 `.exe` 文件后双击运行，或添加至系统环境变量中使用。

## 💡 项目特点

- 🕒 每日定时自动同步
- 🌍 解决 GitHub 官方源访问缓慢或下载失败问题
- 💼 支持多系统多架构
- 🚀 可用于本地部署或搭建私有镜像站点

## 🔐 权限说明

- 本项目使用 GitHub Actions 自动创建 Release，需要配置 `secrets.RELEASE_TOKEN`，可使用具有 `repo` 权限的 GitHub Personal Access Token（PAT）。

------

欢迎 Star 支持该项目！如有建议或问题欢迎提交 Issue 🙌

