### ⚠️ this method does not work on iOS 15+ and this repo won't be updated anytime soon. ⚠️
last updated: 18 January 2024

# 💡 iOS 64 bit dual boot guide (only vulnerable to checkm8 devices are supported)
this is a little repo that contains everything you need to dual boot your 64 bit iPhone, iPad or iPod Touch with unsigned iOS versions (only vulnerable to checkm8 devices can be dual booted for now) without blobs shsh2. if you want to dual boot a 32 bit device, search for a guide about CoolBooter. this tutorial is valid only for macOS users.

## 📮 if you have an unsupported device / iOS version
note that this method doesn't work on iOS 15+, so this guide won't be updated anymore. despite that, you still have some chances to dualboot your device with other iOS versions:
- if you're on iOS 15.x you can dualboot with tools like [dualra1n](https://github.com/edwin170/dualra1n) or [seprmvr64](https://github.com/mineek/seprmvr64)
  - you must have a [compatible chip](#compatible-chips)
- if you're on iOS 16+, there are no methods for that right now. i'll try to update this giude whenever there will be a new method.

you can find out if your device is compatible with this procedure based on its chip. you can simply search on internet what is the chip of your device and check if your chip is into this list.

### compatible chips
A7(X), A8(X), A9(X), A10(X), A11. They must be on iOS 14.X or lower.

**IMPORTANT:** on A11 devices (like the iPhone 8(+) or X) a variety of incompatibility problems may occur, like the breaking of the Touch/Face ID. try it at your own risk.

before starting, you also need to verify if the SEP of your iOS version (installed right now) is compatible with the version of iOS you want to dual boot. you can do this checking [this file](https://docs.google.com/spreadsheets/d/1Mb1UNm6g3yvdQD67M413GYSaJ4uoNhLgpkc7YKi3LBs/). finally, the last thing you have to verify is if you’re in a jailbreakkable version of iOS 14 or older.

done all this, you’re ready to start! the first thing you have to do is…

## 1. JAILBREAK YOUR DEVICE
for this step, you need to install checkra1n on your mac, and you have to jailbreak your device. you can find checkra1n [here](https://checkra.in/).

## 2. DOWNLOAD AND SETUP DIVISÉ
Divisé is a powerful iOS tweak made by [MatthewPierson](https://github.com/MatthewPierson). it allows you to easily prepare your checkm8 vulnerable device to boot the second OS. download the tweak from the [Dynastic Repo](https://repo.dynastic.co/), open the new Divisé app appeared on your home screen, select the Dual boot option and then, after the explain, click on Download IPSW. you must select an iOS version compatible with your SEP (i know, it’s a big limitation). once you’ve done this, you need to attend the finish of the process (it may take some time), and at the end, click Back on the popup and after click on Dual boot device. give all the needed confirms, and when the process is done, you can finally proceed to boot the second OS! do not click reboot on the popup, but read directly the next step of the process.

**IMPORTANT:** remember what disk is indicated to you by the popup (ex *disk0s1s4*).

## 3. ENTER PWNDFU MODE
you have to put your device into a special DFU mode called PWNDFU mode. the process for this step is different for each chip. you can download a cool tool that automates this process for you by clicking [here](https://github.com/ddvniele/iOS-64bit-dualboot-guide/releases/download/pwndfu-exploit/pwndfu.zip). you just have to download the ZIP file, extract it and read the content of the "Tutorial Open Tool.txt" file to understand how can you open it. now connect your device (already put into DFU mode) to your mac and start the process of entering pwndfu mode keeping the "Auto" option selected (unless you already know how to do it with the other options, that will let you save a bit of tries). If the process fail, just repeat it again. It's not a very reliable process and it's common to fail at the first tries. you can also try to unplug and then re-enter DFU mode before repeating the process. Years ago, there was a very simple (and i'd say better) guide linked here, but it seems that it's no longer online.

## 4. DOWNLOAD ON YOUR MAC THE IPSW FILE
you must download on your mac the iPSW file for the iOS version you chose on Divisé. on [this page](https://ipsw.me/), select your device model and download the right file.

## 5. BOOT THE 2ND OS WITH RAMIEL
Ramiel is another tool made by [MatthewPierson](https://github.com/MatthewPierson) that you can [download here](https://ramiel.app/). Install it on your mac, open it, download all the necessary components and click on Advanced. select Boot Dualbooted OS, click on it and write the number of the disk that appeared on the Divisé popup before entering in PWNDFU mode. click now yes on each popup and now you can close the settings. you can finally click on Boot Device. click now on Run checkm8 and attend. this step is very critic for the process. in most cases, it will fail. if it happen, try again until it goes. Select now the iPSW file previously downloaded and wait for the process to finish.

if all went well, your device should have booted into the dual boot partition. have fun with your 2nd OS!

## VERY IMPORTANT!!
remember to not set a passcode at the 2nd OS!! it will break the booting of the partition. remember also to not erase the content of the 2nd OS from the settings.

**IMPORTANT:** when you will reboot your device, it will revert to the original iOS version. to boot again the 2nd OS, you have to re-jailbreak your device, open Divisé, click on Manage Dualboot, click on Mount the 2nd os, re-put your device in PWNDFU mode, re-open Ramiel and re-do the booting process.
