# Bonjour/MDNS on Appveyor

If you want to test MDNS or other Apple protocol stuff or Homekit you need additional files installed. They are all contained in the bonjour sdk, so install it in your appveyor.yml:

```
install:
  - appveyor DownloadFile https://github.com/Apollon77/SupportingFiles/raw/master/appveyor/bonjour/bonjourcore2.msi
  - msiexec /i bonjourcore2.msi /qn
  - del bonjourcore2.msi
  - appveyor DownloadFile https://github.com/Apollon77/SupportingFiles/raw/master/appveyor/bonjour/bonjoursdksetup.exe
  - bonjoursdksetup.exe /quiet
  - del bonjoursdksetup.exe
  - set BONJOUR_SDK_HOME=C:\Program Files\Bonjour SDK
```
