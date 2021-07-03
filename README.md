# Make-Me-Xfce /// Ubuntu Server ARM64 /// Raspberry Pi 4
### This is just an experiment !!!!
![Logo](Screenshot_2021-07-03_00-54-22.png)   



### For 4 months I tried to make a stable Ubuntu based system without Gnome and finaly it worked.     
### Read a lot nothing was convincing... But Now it's stabel    

>https://github.com/novaspirit/rpi_ubu64_desktop

>https://www.liquidweb.com/kb/install-xfce-desktop-environment-on-ubuntu-16-04/

>https://linuxconfig.org/install-xfce-xubuntu-desktop-on-ubuntu-20-04-focal-fossa-linux

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

###Numix Icon Theme
```
sudo apt install numix-icon-theme-circle

```

###Fancy Menu

```
sudo apt install gnome-pie
```
