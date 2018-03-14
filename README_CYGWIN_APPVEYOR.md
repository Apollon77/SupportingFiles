# Cygwin on Appveyor

Cygwin is already installed on Appveyor in general. Here are some usefull commands for your appveyor.yml:

## Update Cygwin to current version
```
install:
  - appveyor DownloadFile https://cygwin.com/setup-x86.exe -FileName C:\cygwin\setup-x86.exe
  - C:\cygwin\setup-x86.exe -qnNdO -R C:/cygwin -s http://cygwin.mirror.constant.com -l C:/cygwin/var/cache/setup
```

## Install additional Cygwin packages
... like socat
```
install:
  - C:\cygwin\setup-x86.exe -qnNdO -R C:/cygwin -s http://cygwin.mirror.constant.com -l C:/cygwin/var/cache/setup -P socat
```
