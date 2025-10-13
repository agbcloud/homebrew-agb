# AGB Cloud Homebrew Tap

这是 AGB Cloud 的官方 Homebrew tap，提供便捷的 AGB 命令行工具安装方式。

## 快速安装

### 方法一：通过 Tap 安装（推荐）

```bash
# 1. 添加 AGB Cloud 的 Homebrew tap
brew tap agbcloud/agb

# 2. 安装 agb 命令行工具
brew install agb

# 3. 验证安装
agb version
```

## 使用方法

安装完成后，您可以使用以下命令：

```bash
# 查看版本信息
agb version

# 查看帮助信息
agb --help

# 使用 AGB 命令
agb [command] [options]
```

## 更新和卸载

### 更新到最新版本

```bash
# 更新 Homebrew 和所有包
brew update && brew upgrade

# 或者只更新 agb
brew upgrade agb
```

### 卸载

```bash
# 卸载 agb
brew uninstall agb

# 移除 tap（可选）
brew untap agbcloud/agb
```

## 项目信息

- **项目主页**: https://github.com/litiantian123-code/agbcloud-cli
- **当前版本**: v1.1.7
- **许可证**: MIT
- **描述**: Secure infrastructure for running AI-generated code

## 故障排除

### 常见问题

1. **安装失败**
   ```bash
   # 更新 Homebrew
   brew update
   
   # 清理缓存
   brew cleanup
   
   # 重新安装
   brew reinstall agb
   ```

2. **网络问题（特别是中国用户）**
   
   Formula 已经配置了中国镜像源，如果仍有问题：
   ```bash
   # 设置 Go 代理
   export GOPROXY=https://goproxy.cn,direct
   export GOSUMDB=sum.golang.google.cn
   
   # 重新安装
   brew reinstall agb
   ```

3. **权限问题**
   ```bash
   # 修复 Homebrew 权限
   sudo chown -R $(whoami) $(brew --prefix)/*
   ```

## 开发者信息

### 本地测试

如果您想在本地测试或开发：

```bash
# 克隆仓库
git clone https://github.com/agbcloud/homebrew-agb.git
cd homebrew-agb

# 本地安装测试
brew install --build-from-source ./Formula/agb.rb

# 测试功能
agb version
agb --help

# 卸载测试版本
brew uninstall agb
```

### Formula 文件说明

`Formula/agb.rb` 包含：
- **构建依赖**: Go 语言环境
- **网络优化**: 配置了中国镜像源以提高下载速度
- **版本信息**: 自动注入版本号、Git提交和构建时间
- **测试用例**: 验证安装和基本功能

## 支持

如果您遇到问题：

- 查看 [Issues](https://github.com/agbcloud/homebrew-agb/issues)
- 创建新的 Issue 报告问题
- 查看 [AGB CLI 项目](https://github.com/litiantian123-code/agbcloud-cli)

## 相关链接

- [Homebrew 官网](https://brew.sh/)
- [AGB CLI 项目](https://github.com/litiantian123-code/agbcloud-cli)
- [Homebrew Tap 文档](https://docs.brew.sh/Taps)