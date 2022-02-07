# ARCH LINUX

## DOCKER

```sudo groupadd docker
sudo usermod -aG docker your-user-name
systemctl start docker
sudo chmod 777 /var/run/docker.sock
```

## CHROME_EXECUTABLE

`sudo ln -s /usr/bin/google-chrome-stable /usr/bin/google-chrome`

## BSPWM

```sudo pacman -S xorg-xinit bspwm sxhkd dmenu nitrogen picom xfce4-terminal arandr
mkdir .config/bspwm
mkdir .config/sxhkd
cp /usr/share/doc/bspwm/examples/bspwmrc .config/bspwm/
cp /usr/share/doc/bspwm/examples/sxhkdrc .config/sxhkd/
nano .config/sxhkd/sxhkdrc
cp /etc/X11/xinit/xinitrc .xinitrc
sudo nano .xinitrc
sudo nano /etc/xdg/picom.conf
nitrogen
yay -S polybar pacman-contrib ttf-font-awesome siji-git pulseaudio alsa-utils
mkdir .config/polybar
nano ./config/polybar/config
[Polybar](https://github.com/siduck76/bspwm-dotfiles/tree/main/polybar "bspwm dotfiles")
nano ./config/polybar/launch.sh
```

## TAIWAN MIRRORS

Server = http://archlinux.ccns.ncku.edu.tw/archlinux/$repo/os/$arch <br />
Server = http://free.nchc.org.tw/arch/$repo/os/$arch <br />
Server = https://free.nchc.org.tw/arch/$repo/os/$arch <br />
Server = http://archlinux.cs.nctu.edu.tw/$repo/os/$arch <br />
Server = http://shadow.ind.ntou.edu.tw/archlinux/$repo/os/$arch <br />
Server = https://shadow.ind.ntou.edu.tw/archlinux/$repo/os/$arch <br />
Server = http://ftp.tku.edu.tw/Linux/ArchLinux/$repo/os/$arch <br />
Server = http://ftp.yzu.edu.tw/Linux/archlinux/$repo/os/$arch <br />
Server = https://ftp.yzu.edu.tw/Linux/archlinux/$repo/os/$arch <br />

## OFFICIAL REPO

sudo pacman -S kate konsole netbeans neofetch htop dolphin latte-dock bleachbit gwenview kcalc kdeconnect kdenlive ksysguard okular partitionmanager gparted spectacle qbittorrent libreoffice-still firefox thunderbird ttf-fira-code youtube-dl dart caprine flameshot gamemode mpv zsh-autosuggestions zsh-syntax-highlighting zsh-theme-powerlevel10k zsh-completions linux-lts gnome-keyring zip ark firewalld virtualbox elisa xf86-video-amdgpu noto-fonts-emoji vlc simplescreenrecorder kitty nemo warpinator ark pulseaudio-bluetooth zsh-history-substring-search youtube-dl cmatrix wireshark-qt foliate linux-zen audacious obs-studio

sudo pacman -S gnome

sudo pacman -S php xampp

## MULTILIB

sudo pacman -S wine-gecko wine-mono winetricks steam-native-runtime steam wine

## LUTRIS

sudo pacman -S xdelta3 lutris zenity python-magic

sudo pacman -S lib32-mesa vulkan-radeon lib32-vulkan-radeon vulkan-icd-loader lib32-vulkan-icd-loader

## MISSING FIRMWARE

yay -S aic94xx-firmware wd719x-firmware

## AUR

yay -S pamac-aur google-chrome android-studio nodejs-nativefier visual-studio-code-bin zoom ttf-ms-fonts inxi discord_arch_electron etcher-bin android-sdk-platform-tools nohang-git flutter linux-wifi-hotspot scrcpy update-grub spotify spotify-adblock-git downgrade proton-ge-custom-bin shell-color-scripts xampp

yay -S ms-office-online

## VIRTUALBOX

sudo pacman -S linux-headers

yay -S virtualbox-ext-oracle

## GENYMOTION

yay -S genymotion <br />
sudo vboxreload <br />

## XAMPP

sudo xampp start <br />
sudo xampp stop <br />
sudo xampp restart <br />

## MANJARO

## MIC

'/etc/pulse/daemon.conf’ <br />
avoid-resampling = false <br />
default-sample-rate = 44100 <br />

## PACKET TRACER

curl -s https://raw.githubusercontent.com/marcelobaptista/packettracer/master/install_pt.sh | sudo bash <br />

## GIT PUSH

### Create a new repository on the command line

echo "# myself-html" >> README.md <br />
git init <br />
git add README.md <br />
git commit -m "first commit" <br />
git branch -M master <br />
git remote add origin https://github.com/ZyArko/practice.git <br />
git push -u origin master <br />

### Push an existing repository from the command line

git remote add origin https://github.com/ZyArko/practice.git <br />
git branch -M master <br />
git push -u origin master <br />

## SCRCPY

Installing app/scrcpy to /home/apple/aur/scrcpy/pkg/scrcpy/usr/bin <br />
Stripping target 'app/scrcpy' using strip. <br />
Installing server/scrcpy-server to /home/apple/aur/scrcpy/pkg/scrcpy/usr/share/scrcpy <br />
Installing /home/apple/aur/scrcpy/src/scrcpy-1.16/app/scrcpy.1 to /home/apple/aur/scrcpy/pkg/scrcpy/usr/share/man/man1 <br />

## GAMEMODE

systemctl --user enable gamemoded

## POWERLEVEL10K

git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ~/powerlevel10k <br />
echo 'source ~/powerlevel10k/powerlevel10k.zsh-theme' >>! ~/.zshrc <br />

## SQL SERVER

clone the mssql-sqlserver, msodbcsql , mssql-tools <br />
activate the license <br />
12345 #administrator password <br />
systemctl enable mssql-server # start for the mean time. <br />
systemctl enable mssql-server # start on boot #dont sudo <br />
systemctl enable mssql-server # status <br />
sqlcmd #list of commands <br />
use mssql server in vs code <br />

## PACMAN MIRRORS

sudo pacman -R package_name # -R to remove the application

sudo reflector --latest 5 --sort rate --save /etc/pacman.d/mirrorlist # ARCH

sudo pacman-mirrors --fasttrack 5 && sudo pacman -Syyu # MANJARO

pacman-mirrors --get-branch # GET BRANCH

sudo pacman-mirrors --continent && sudo pacman -Syyu # COUNTRY REPO

sudo pacman-mirrors --geoip && sudo pacman -Syyu #CONTRY REPO

sudo pacman-mirrors --country all --api --protocols all --set-branch stable && sudo pacman -Syyu # RESET MIRRORS

## YAY

yay package_name # search the package name in aur <br />
yay -Ss package_name # search the package name both aur and pamac <br />
yay -S package_name # install package <br />
yay -Sua # update <br />

## OH MY ZSH GIT

/usr/share/oh-my-zsh/tools/install.sh <br />
You have to execute 'cp /usr/share/oh-my-zsh/zshrc ~/.zshrc' to use it add zsh-theme-powerlevel10k ZSH_THEME="powerlevel10k/powerlevel10k" add plugins=git zsh-autosuggestions zsh-syntax-highlighting <br />

## TLP

systemctl status tlp // to open tlp <br />
sudo tlp-stat <br />

Notice: tlp.service is not enabled -- invoke "systemctl enable tlp.service" to correct this! <br />
Notice: tlp-sleep.service is not enabled -- invoke "systemctl enable tlp-sleep.service" to correct this! <br />
Notice: systemd-rfkill.service is not masked -- invoke "systemctl mask systemd-rfkill.service" to correct this! <br />
Notice: systemd-rfkill.socket is not masked -- invoke "systemctl mask systemd-rfkill.socket" to correct this! <br />

## GIT

sudo nano /etc/makepkg.conf # to enabling parallel compiling on your system to improve the compiling speed <br />
CTRL + W, you can search for a term MAKEFLAGS then hit enter. <br />
The variable $(nproc) will define a number of available threads in your processor automatically. <br />

## INSTALL GIT REPOSITORY

git clone htps://aur.archlinux.org/spotify.git <br />
ls <br />
cd spotify <br />
check PKGBUILD <br />
makepkg -si or -sia #to compile and install the program <br />

## UPDATE GRUB

grub-mkconfig -o /boot/grub/grub.cfg

## INTRO IN ARCH

dont add plasma-application <br />
add konsole, kate, cronie and timeshift, to setup first <br />

## WINE

Run 'systemctl restart systemd-binfmt' in order to make the wine binfmt available on your system.

## VIRTUALBOX

===> You must load vboxdrv module before starting VirtualBox: <br />
===> # modprobe vboxdrv <br />
sudo vboxreload # reboot virtualbox module to the kernel <br />
https://wiki.manjaro.org/index.php?title=Virtualbox //virtualbox installation <br />

## OPENSDK

Configuring java-runtime-common... <br />
For the complete set of Java binaries to be available in your PATH, <br />
you need to re-login or source /etc/profile.d/jre.sh <br />
Please note that this package does not support forcing JAVA_HOME as former package java-common did <br />
Configuring jre-openjdk... <br />
when you use a non-reparenting window manager, <br />
set \_JAVA_AWT_WM_NONREPARENTING=1 in /etc/profile.d/jre.sh <br />

## WARPINATOR

systemctl start sshd

> and then verify 22 is listening with that same netstat command.

## WINETRICKS

`cd wine`

> wine bottle

`WINEARCH=win32 WINEPREFIX=~/wine/winebottle winetricks`

`WINEARCH=win32 WINEPREFIX=~/wine/winebottle wine ~/wine/winebottle/drive_c/testprogram.exe`

> to execute direct into drive c

`wine ./setup.exe`

> to install ms office 2013

## ARDUINO

Add yourself to the uucp group to access the serial ports: <br />
sudo usermod -a -G uucp <user> <br />
Please checkout the wiki for further information. <br />

## WPS OFFICE

ATTENTION: When you shut down wps, the wpsoffice process may still exist. <br />
You can do 'sudo chmod -x /usr/lib/office6/wpsoffice' to fix it. But <br />
this might bring you problem with signing in. <br />

## FREE OFFICE

035316509684 //Free Office Product Key

## WEBDEV SERVE FOR DART

export PATH="$PATH":"$HOME/.pub-cache/bin"

## WINE

Run 'systemctl restart systemd-binfmt' in order to make the wine binfmt available on your system. <br />

## FIREWALLD

systemctl start firewalld # start the service for the mean time <br />
systemctl enable firewalld # enable the service to auto-start at boot time <br />
systemctl status firewalld # view service status <br />

## XAMPP

XAMPP is now installed below the /opt/lampp directory <br />
To start, stop or restart XAMPP simply call the command: <br />
lampp {start, stop, restart} or xampp {start, stop, restart} <br />
Then you can check that everything really works, <br />
Just enter the following URL at your web browser: http://localhost <br />

## COMMANDS

inxi -Fxzc0 //specs <br />
sudo pacman -Syu // to update arch base <br />
acpi_backlight=vendor // backlight error in boot <br />
sudo update-grub // to update grub <br />

## TOR BROWSER

edit /etc/apparmor.d/local/torbrowser.Browser.firefox and add the following line: <br />
owner /{dev,run}/shm/org.mozilla._._ rw, <br />
Also add exactly the same line to /etc/apparmor.d/local/torbrowser.Browser.plugin-container. <br />
Then: sudo systemctl restart apparmor <br />

## INSTALLING FLUTTER

groupadd flutterusers <br />
gpasswd -a apple flutterusers <br />
chown -R :flutterusers /opt/flutter <br />
chmod -R g+w /opt/flutter <br />
newgrp flutterusers <br />
export PATH="$PATH":"opt/flutter/bin" <br />

## ANDROID STUDIO

sudo chmod -R 777 /opt/android-sdk

# DEBIAN

## SNAP

sudo apt update <br />
sudo apt install -y snap <br />
sudo snap install hello-world(name) <br />

## GUI Laptop Mode Tools:

sudo lmt-config-gui

## XAMPP

XAMPP: // lampp need to access as root folder then exec manager-linux-x64.run <br />
sudo chmod 777 -R /opt/lampp/htdocs <br />
sudo chmod 755 /opt/lampp/phpmyadmin/config.inc.php <br />

## COMMANDS IN DEB

sudo apt update // check the updates <br />
sudo apt upgrade // to update deb <br />
sudo apt-get autoclean // You can clean partial packages using a command <br />
sudo apt-get clean // You can auto cleanup apt-cache <br />
sudo apt-get autoremove // You can clean up of any unused dependencies <br />

## VIDEO CARD (GPU) MEMORY RAM SIZE

lspci // use string called devices in the specified domain <br />
lspci | grep VGA // or open specific VGA <br />
lspci -v -s 03:00.0 // Raven Rige <br />
neofetch <br />
htop <br />

## PERMISSION

sudo chmod -R 777 /home/sixven/camp_sms/inputs //for change the permission of the folder <br />
sudo cp -r (your current folder directory) (file directory of where you want to copy the file) // For example : If you are copying file from downloads to boot folder then type //For copying the files of with permission <br />
sudo cp -r /home/lw/Downloads/sampleImage.png boot/themes <br />

```

```
