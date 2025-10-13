# AGB Cloud Homebrew Tap

这是 AGB Cloud 的官方 Homebrew tap，提供便捷的 AGB 命令行工具安装方式。

## 安装步骤

### 1. 添加 Tap

首先，将此 tap 添加到您的 Homebrew：

```bash
brew tap agbcloud/agbcloud-homebrew
```

### 2. 安装 AGB

添加 tap 后，您可以直接安装 AGB：

```bash
brew install agb
```

## 使用方法

安装完成后，您可以使用以下命令：

```bash
# 查看版本
agb --version

# 查看帮助
agb --help

# 使用 AGB 命令
agb [command] [options]
```

## 更新和卸载

### 更新到最新版本

```bash
brew update
brew upgrade agb
```

### 卸载

```bash
# 卸载 AGB
brew uninstall agb

# 移除 tap（可选）
brew untap agbcloud/agbcloud-homebrew
```

## 故障排除

### 常见问题

1. **安装失败**
   ```bash
   # 尝试更新 Homebrew
   brew update
   
   # 清理缓存
   brew cleanup
   
   # 重新安装
   brew reinstall agb
   ```

2. **权限问题**
   ```bash
   # 修复权限
   sudo chown -R $(whoami) $(brew --prefix)/*
   ```

3. **依赖问题**
   ```bash
   # 检查依赖
   brew deps agb
   
   # 安装缺失的依赖
   brew install <missing-dependency>
   ```

## 开发者信息

### 本地开发

如果您想在本地开发或测试 formula：

```bash
# 克隆仓库
git clone https://github.com/agbcloud/agbcloud-homebrew.git
cd agbcloud-homebrew

# 本地安装
brew install --build-from-source ./Formula/agb.rb
```

### 贡献指南

我们欢迎社区贡献！请遵循以下步骤：

1. Fork 此仓库
2. 创建功能分支 (`git checkout -b feature/amazing-feature`)
3. 提交更改 (`git commit -m 'Add some amazing feature'`)
4. 推送到分支 (`git push origin feature/amazing-feature`)
5. 创建 Pull Request

### Formula 规范

在创建或更新 formula 时，请确保：

- 遵循 [Homebrew Formula Cookbook](https://docs.brew.sh/Formula-Cookbook)
- 包含适当的测试用例
- 提供准确的软件包描述和主页链接
- 验证 SHA256 校验和的正确性

## 支持

如果您遇到问题或有疑问：

- 查看 [Issues](https://github.com/agbcloud/agbcloud-homebrew/issues)
- 创建新的 Issue 来报告问题或请求功能
- 查看 [Homebrew 官方文档](https://docs.brew.sh/)

## 许可证

本项目采用 MIT 许可证 - 查看 [LICENSE](LICENSE) 文件了解详情。

## 相关链接

- [Homebrew 官网](https://brew.sh/)
- [Homebrew Tap 文档](https://docs.brew.sh/Taps)
- [Formula Cookbook](https://docs.brew.sh/Formula-Cookbook)
- [AGB 项目主页](https://github.com/agbcloud/agbcloud-cli)

