# AGB Cloud Homebrew Tap

This is the official Homebrew tap for AGB Cloud, providing a convenient way to install the AGB command-line tool.

## Quick Installation

### Install via Tap (Recommended)

```bash
# 1. Add AGB Cloud's Homebrew tap
brew tap agbcloud/agb

# 2. Install agb command-line tool
brew install agb

# 3. Verify installation
agb version
```

## Usage

After installation, you can use the following commands:

```bash
# Check version information
agb version

# View help information
agb --help

# Use AGB commands
agb [command] [options]
```

## Update and Uninstall

### Update to Latest Version

```bash
# Update Homebrew and all packages
brew update && brew upgrade

# Or update only agb
brew upgrade agb
```

### Uninstall

```bash
# Uninstall agb
brew uninstall agb

# Remove tap (optional)
brew untap agbcloud/agb
```

## Project Information

- **Project Homepage**: https://github.com/agbcloud/agbcloud-cli
- **Current Version**: v0.1.0
- **License**: MIT
- **Description**: Secure infrastructure for running AI-generated code

## Troubleshooting

### Common Issues

1. **Installation Failed**
   ```bash
   # Update Homebrew
   brew update
   
   # Clean cache
   brew cleanup
   
   # Reinstall
   brew reinstall agb
   ```

2. **Network Issues (Especially for Chinese Users)**
   
   The Formula has been configured with Chinese mirror sources. If you still have issues:
   ```bash
   # Set Go proxy
   export GOPROXY=https://goproxy.cn,direct
   export GOSUMDB=sum.golang.google.cn
   
   # Reinstall
   brew reinstall agb
   ```

3. **Permission Issues**
   ```bash
   # Fix Homebrew permissions
   sudo chown -R $(whoami) $(brew --prefix)/*
   ```

## Developer Information

### Local Testing

If you want to test or develop locally:

```bash
# Clone repository
git clone https://github.com/agbcloud/homebrew-agb.git
cd homebrew-agb

# Local installation test
brew install --build-from-source ./Formula/agb.rb

# Test functionality
agb version
agb --help

# Uninstall test version
brew uninstall agb
```

### Formula File Description

`Formula/agb.rb` contains:
- **Build Dependencies**: Go language environment
- **Network Optimization**: Configured with Chinese mirror sources to improve download speed
- **Version Information**: Automatically injects version number, Git commit, and build time
- **Test Cases**: Validates installation and basic functionality

## Support

If you encounter issues:

- Check [Issues](https://github.com/agbcloud/homebrew-agb/issues)
- Create a new Issue to report problems
- View [AGB CLI Project](https://github.com/litiantian123-code/agbcloud-cli)

## Related Links

- [Homebrew Official Website](https://brew.sh/)
- [AGB CLI Project](https://github.com/agbcloud/agbcloud-cli)
- [Homebrew Tap Documentation](https://docs.brew.sh/Taps)