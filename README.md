# Qinglong Debian Image Auto Retagger

该项目每天自动检查 Qinglong 最新版本号，并将 `whyour/qinglong:debian` 镜像打上对应的 `版本号-debian` 标签，上传至你的 Docker Hub 仓库中。

## 示例

| 来源镜像 | 目标镜像 |
|----------|----------|
| `whyour/qinglong:debian` | `yourname/qinglong:2.19.2-debian` |

## 📦 功能

- 每天自动获取 Qinglong 最新版本
- 检查是否已存在该 `*-debian` 标签
- 若不存在，复制 `debian` 镜像并推送

## 🔧 设置

1. Fork 本仓库
2. 添加 GitHub Secrets：

| 名称 | 描述 |
|------|------|
| `DOCKER_USERNAME` | 你的 Docker Hub 用户名 |
| `DOCKER_PASSWORD` | Docker Hub 密码或 Access Token |

3. 可手动触发工作流或等待自动运行（每天 2 点 UTC）
