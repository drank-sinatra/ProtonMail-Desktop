# ProtonMail Desktop
- - - -

## Preface
ProtonMail is designed to be used as a web application in order to maintain the integrity of the messages contained in one’s account. Proton does of course have the bridge client for macOS and Windows, but this opens users up to inadvertent data exfiltration as there are now local copies of messages in the user’s chosen desktop email application. This application is built using [Nativefier](https://github.com/jiahaog/Nativefier), which leverages [Electron](https://www.electronjs.org/) to wrap any web app into a desktop version for Windows, macOS, and Linux. The benefit to this vice Proton’s bridge is that no local copies of messages are stored whilst allowing for a traditional email client feel with desktop notifications and the like. 

## Build
This version leverages ProtonMail Beta in order to allow dark mode in ProtonMail’s interface as well as the advanced features like spam sweeping.
> **Note**: Including the icon is not required, but makes it more pleasant on macOS.  

**macOS**
```
nativefier -p mac -a x64 https://beta.protonmail.com --counter --darwin-dark-mode-support --single-instance -i ~/gits/ProtonMail/Resources/ProtonMail.png -n ProtonMail
```

**Linux (x64)**
```
nativefier -p linux -a x64 https://beta.protonmail.com --counter --tray --single-instance -i ~/gits/ProtonMail/ProtonMail.png -n ProtonMail
```
**Linux (ARM)**
```
nativefier -p linux -a arm https://beta.protonmail.com --counter --tray --single-instance -i ~/gits/ProtonMail//ProtonMail.png -n ProtonMail
```
**Linux (ARM64)**
```
nativefier -p linux -a ARM64 https://beta.protonmail.com --counter --tray --single-instance -i ~/gits/ProtonMail//ProtonMail.png -n ProtonMail
```
