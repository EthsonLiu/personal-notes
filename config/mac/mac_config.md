## 目录

- [homebrew](#homebrew)
- [consolas](#consolas)

## homebrew

```shell
cd ~
curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install >> brew_install
vim brew_install
```

修改为

```
#!/System/Library/Frameworks/Ruby.framework/Versions/Current/usr/bin/ruby
# This script installs to /usr/local only. To install elsewhere you can just
# untar https://github.com/Homebrew/brew/tarball/master anywhere you like or
# change the value of HOMEBREW_PREFIX.
HOMEBREW_PREFIX = "/usr/local".freeze
HOMEBREW_REPOSITORY = "/usr/local/Homebrew".freeze
HOMEBREW_CACHE = "#{ENV["HOME"]}/Library/Caches/Homebrew".freeze
HOMEBREW_OLD_CACHE = "/Library/Caches/Homebrew".freeze
#BREW_REPO = "https://github.com/Homebrew/brew".freeze
BREW_REPO = "https://mirrors.aliyun.com/homebrew/brew.git".freeze # 这里
#CORE_TAP_REPO = "https://github.com/Homebrew/homebrew-core".freeze
CORE_TAP_REPO = "https://mirrors.aliyun.com/homebrew/homebrew-core.git".freeze # 这里可能已经没有了
``

修改好之后，按 ESC，输入 :wq 保存退出，执行 brew_install，

```shell
/usr/bin/ruby ~/brew_install
```

1. 替换 homebrew 默认源

```shell
cd "$(brew --repo)"
git remote set-url origin https://mirrors.aliyun.com/homebrew/brew.git
```

2. 替换 homebrew-core 源

```shell
cd "$(brew --repo)/Library/Taps/homebrew/homebrew-core"
git remote set-url origin https://mirrors.aliyun.com/homebrew/brew.git
```

3. 更新 brew

```shell
brew update
```

## consolas

参考：<https://gist.github.com/avalonalex/8125197>

```shell
# Thanks to this post:
# http://blog.ikato.com/post/15675823000/how-to-install-consolas-font-on-mac-os-x

brew install cabextract
cd ~/Downloads
mkdir consolas
cd consolas
curl -O https://sourceforge.net/projects/mscorefonts2/files/cabs/PowerPointViewer.exe
cabextract PowerPointViewer.exe
cabextract ppviewer.cab
open CONSOLA*.TTF
```