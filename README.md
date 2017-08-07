# MacInitSSH
## 安装brew

```bash
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew doctor
brew update
```

## 安装node
```bash
brew install node
```

## 安装zsh

```bash
brew install wget
wget https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh -O - | sh
chsh -s /bin/zsh
open .zshrc #修改如下内容
plugins=(git sublime ruby autojump osx)
```

## 安装ruby

```bash
brew install rbenv ruby-build
# Add rbenv to bash so that it loads every time you open a terminal
echo 'if which rbenv > /dev/null; then eval "$(rbenv init -)"; fi' >> ~/.zshrc
source ~/.zshrc
# Install Special Version Ruby
rbenv install 2.3.0 #替换成最新版本号
rbenv global 2.3.0 #替换成最新版本号
ruby -v
```

## 安装 cocoapods

```bash
#gem sources --remove https://rubygems.org/ ＃移除官方源
#gem sources -a https://ruby.taobao.org/ ＃添加淘宝源
#gem sources -l ＃列出当前的源
sudo gem install -n /usr/local/bin cocoapods -v 1.2.1 #替换成最新版本号
```

```
# 设置并发数
sudo ulimit -n 12100 
# Enable repeat on keydown
defaults write -g ApplePressAndHoldEnabled -bool false
# Use current directory as default search scope in Finder
defaults write com.apple.finder FXDefaultSearchScope -string "SCcf"
# Show Path bar in Finder
defaults write com.apple.finder ShowPathbar -bool true
# Show Status bar in Finder
defaults write com.apple.finder ShowStatusBar -bool true
# Show indicator lights for open applications in the Dock
defaults write com.apple.dock show-process-indicators -bool true
# Enable AirDrop over Ethernet and on unsupported Macs running Lion
# defaults write com.apple.NetworkBrowser BrowseAllInterfaces -bool true
#Set a blazingly fast keyboard repeat rate
defaults write NSGlobalDomain KeyRepeat -int 0.02
#Set a shorter Delay until key repeat
defaults write NSGlobalDomain InitialKeyRepeat -int 12
#Enable Safari’s debug menu
# defaults write com.apple.Safari IncludeInternalDebugMenu -bool true
#Add a context menu item for showing the Web Inspector in web views
# defaults write NSGlobalDomain WebKitDeveloperExtras -bool true
#Show the ~/Library folder
chflags nohidden ~/Library

defaults write com.apple.desktopservices DSDontWriteNetworkStores -bool TRUE

