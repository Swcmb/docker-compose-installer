# Docker Compose 国内安装包

解决Docker Compose国内网络问题，自动同步官方安装包到Release

## 特点
- 使用Github Action将官网的安装包定时下载到本项目Release，供国内使用
- 官方安装包，安全可靠
- 每天自动定时同步，保证最新

## Docker Compose安装

### Linux
一键安装命令
```bash
# 下载最新版Docker Compose
sudo curl -fsSL https://github.com/Swcmb/docker-compose-installer/releases/download/latest/docker-compose-Linux-x86_64 -o /usr/local/bin/docker-compose
# 添加执行权限
sudo chmod +x /usr/local/bin/docker-compose
# 验证安装
docker-compose --version
```

### Windows
1. 下载Windows版本安装包，进入本项目的Release
   https://github.com/Swcmb/docker-compose-installer/releases
2. 下载docker-compose-Windows-x86_64.exe文件
3. 将文件重命名为docker-compose.exe并添加到系统PATH路径中
4. 在命令提示符中验证安装：
   ```cmd
docker-compose --version
```

### Mac
1. 进入本项目的Release，下载Mac系统的安装包
   https://github.com/Swcmb/docker-compose-installer/releases
2. 根据CPU架构选择对应的安装包：
   - Intel芯片: docker-compose-Darwin-x86_64
   - 苹果芯片: docker-compose-Darwin-arm64
3. 将下载的文件移动到/usr/local/bin目录并添加执行权限：
   ```bash
chmod +x docker-compose-Darwin-*
sudo mv docker-compose-Darwin-* /usr/local/bin/docker-compose
```
4. 验证安装：
   ```bash
docker-compose --version
```

## 自动同步说明
本项目使用GitHub Actions每天自动同步Docker Compose官方最新版本，确保提供的安装包始终为最新稳定版。

同步时间：每天UTC时间0点（北京时间早上8点）

## 项目地址
- GitHub: https://github.com/Swcmb/docker-compose-installer