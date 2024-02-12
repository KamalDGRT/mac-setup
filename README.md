# mac-setup

My macOS setup/config.

#### Applications

I install apps predominantly using [HomeBrew](brew.sh).

##### Casks:

I install them using `brew install --cask <package-name>`.

Replace `<package-name>` with one of the following packages below.

1. android-file-transfer
1. android-studio
1. bitwarden
1. brave-browser
1. dbeaver-community
1. discord
1. font-fira-code
1. google-chrome
1. imageoptim
1. libreoffice
1. localsend
1. megasync
1. microsoft-remote-desktop
1. mkvtoolnix
1. opera
1. postman
1. qbittorrent
1. slack
1. sourcetree
1. spotify
1. sublime-text
1. syncthing
1. telegram-desktop
1. the-unarchiver
1. visual-studio-code
1. vlc
1. whatsapp
1. xcodes
1. zerotier-one
1. zoom

#### Binaries

I install them using `brew install <package-name>`.

Replace `<package-name>` with one of the following packages below.

1. ffmpeg
2. gh
3. bison
4. cmake
5. fmt
6. cocoapods
7. neofetch
8. htop
9. mariadb
10. tree
11. pkg-config
12. zsh
13. zsh-autosuggestions
14. zsh-syntax-highlighting
15. yt-dlp

#### MariaDB setup instructions

I am assuming it is a fresh install.

- `brew install bison cmake fmt pkg-config`
- `brew install mariadb`
- `mysql.server start`
- `brew services start mariadb`
- `mysql`

In your shell config (`.bashrc` / `.zshrc` / `.fishrc` / anything else) add this set of lines.
This will help you use `mariadb` in your other applications (espcially Python with `mysqlclient` package).

```sh
# If you need to have bison first in your PATH, run:
export PATH="/opt/homebrew/opt/bison/bin:$PATH"

# For compilers to find bison you may need to set:
export LDFLAGS="-L/opt/homebrew/opt/bison/lib"

# # For pkg-config to find mysql-client you may need to set:
export PKG_CONFIG_PATH=" /opt/homebrew/opt/mariadb/lib/pkgconfig "

# openssl compilation flags
export LDFLAGS="-L$(brew --prefix openssl)/lib"
export CPPFLAGS="-I$(brew --prefix openssl)/include"
```
