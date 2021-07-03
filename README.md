# PiGro-Xf OS /// Ubuntu Server + Xfce + Box86 + Lutris + Bug-Steam xD/// Raspberry Pi 4
### This is just an experiment with a lot trial and error!!!!
![Logo](Screenshot_2021-07-03_00-54-22.png)   



### For 4 months I tried to make a stable Ubuntu based system without Gnome and finaly it worked.     
### Read a lot nothing was convincing... But Now it's stabel    

>https://github.com/novaspirit/rpi_ubu64_desktop    
>https://www.liquidweb.com/kb/install-xfce-desktop-environment-on-ubuntu-16-04/    
>https://linuxconfig.org/install-xfce-xubuntu-desktop-on-ubuntu-20-04-focal-fossa-linux    
>https://itai-nelken.github.io/Ubuntu-on-rpi-fixes/    
>https://github.com/Botspot/pi-apps    


# Instructions

### Clock Settings
/boot/firmware/config.txt

> over_voltage=8    
> arm_freq=2147   
> gpu_freq=750   
> gpu_mem=128   
   
   
### Desktop Installation

```
sudo apt update 

sudo reboot

sudo apt upgrade

sudo apt install tasksel

sudo tasksel 
```

> select xubuntu-desktop

### Add Pi As User

```
sudo adduser pi
```
>Enter Name (Pi) & PW:   
       
    Enter the new value, or press ENTER for the default    
        Full Name []: Pi    
        Room Number []:     
        Work Phone []:     
        Home Phone []:     
        Other []:     
    Is the information correct? [Y/n] Y    


```
sudo adduser pi sudo
```
> Adds root privileges

```
sudo reboot
```

### Round Cornors Panel Edit .config/gtk-3.0/gtk.css
```
touch .config/gtk-3.0/gtk.css
nano .config/gtk-3.0/gtk.css
```
```
.xfce4-panel {
    border-radius: 15px;
}
and then

xfce4-panel -r
```
### Numix Dark Theme

```
wget https://dllb2.pling.com/api/files/download/j/eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpZCI6IjE1OTIxMDI0MDUiLCJ1IjpudWxsLCJsdCI6ImRvd25sb2FkIiwicyI6IjczNTM1MjM5MmNiOTUzZTczMWViMDA5OWQxMmMxN2M1ODdiODgwZTQ1NmY2MTdmNWJjMjMyMGNhOWZhMTI4ODA2NThiZjAyZjc5ODM0NWM4OTg1ZDgyZGM3OGVkNTJiMDJkMjc1MGM1ODczZjE4ZmM1YWVmOTk3ZmUyYjE5MGYzIiwidCI6MTYyNTI3NDI4MCwic3RmcCI6ImNjZGMwOTU5NzUzODk2NTY2ZTVjOTBhYmQ3ZDM5YWQ4Iiwic3RpcCI6IjkyLjIxMi4zOS4yMjkifQ.W-KHajiPU29nGyOt12aPifjI5QeLrnk5uA2JsqN9BLg/Numix-dark.zip
--2021-07-03 00:05:52--  https://dllb2.pling.com/api/files/download/j/eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpZCI6IjE1OTIxMDI0MDUiLCJ1IjpudWxsLCJsdCI6ImRvd25sb2FkIiwicyI6IjczNTM1MjM5MmNiOTUzZTczMWViMDA5OWQxMmMxN2M1ODdiODgwZTQ1NmY2MTdmNWJjMjMyMGNhOWZhMTI4ODA2NThiZjAyZjc5ODM0NWM4OTg1ZDgyZGM3OGVkNTJiMDJkMjc1MGM1ODczZjE4ZmM1YWVmOTk3ZmUyYjE5MGYzIiwidCI6MTYyNTI3NDI4MCwic3RmcCI6ImNjZGMwOTU5NzUzODk2NTY2ZTVjOTBhYmQ3ZDM5YWQ4Iiwic3RpcCI6IjkyLjIxMi4zOS4yMjkifQ.W-KHajiPU29nGyOt12aPifjI5QeLrnk5uA2JsqN9BLg/Numix-dark.zip
```
> mv to .local/share/themes

### Numix Icon Theme
```
sudo apt install numix-icon-theme-circle

```

### Fancy Menu

```
sudo apt install gnome-pie
```


### Box86
```
sudo dpkg --add-architecture armhf

sudo apt update

sudo apt install libc6:armhf  libx11-6:armhf  libgdk-pixbuf2.0-0:armhf libgtk2.0-0:armhf libstdc++6:armhf libsdl2-2.0-0:armhf mesa-va-drivers:armhf libsdl1.2-dev:armhf libsdl-mixer1.2:armhf libpng16-16:armhf libcal3d12v5:armhf libsdl2-net-2.0-0:armhf libopenal1:armhf libsdl2-image-2.0-0:armhf libvorbis-dev:armhf libcurl4:armhf osspd:armhf pulseaudio:armhf libjpeg62:armhf libudev1:armhf libgl1-mesa-dev:armhf libsnappy1v5:armhf libx11-dev:armhf libsmpeg0:armhf libboost-filesystem1.67.0:armhf libboost-program-options1.67.0:armhf libavcodec58:armhf libavformat58:armhf libswscale5:armhf libmyguiengine3debian1v5:armhf libboost-iostreams1.67.0:armhf  libsdl2-mixer-2.0-0:armhf
```
```
sudo apt update

sudo apt  install cmake
sudo apt install make

sudo apt install pulseaudio pulseaudio-utils

wget -qO- https://raw.githubusercontent.com/Botspot/pi-apps/master/install | bash


~/pi-apps/manage install Box86
```


### Steam (totally buggy
```
sudo apt install libnss3:armhf libnm0:armhf libdbus-glib-1-2:armhf libudev1:armhf libnspr4:armhf libgudev-1.0-0:armhf libusb-1.0-0:armhf libappindicator1:armhf

wget https://steamcdn-a.akamaihd.net/client/installer/steam.deb

sudo dpkg -i steam.deb
```
### Lutris
```
sudo add-apt-repository ppa:lutris-team/lutris
sudo apt update
sudo apt install lutris
```
