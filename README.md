# 💡 iOS 64 bit dual boot guide (only vulnerable to checkm8 devices are supported)
hii, this is a little repo that contains everything you need to dual boot your 64 bit iPhone, iPad or iPod Touch with unsigned iOS versions (only vulnerable to checkm8 devices can be dual booted for now) without blobs shsh2. if you want to dual boot a 32 bit device, search for a guide about CoolBooter. this tutorial is valid only for macOS users.

you can find out if your device is compatible with this procedure based on its chip. you can simply search on internet what is the chip of your device and check if your chip is into this list.

**compatible chips are:** A7(X), A8(X), A9(X), A10(X), A11.

**IMPORTANT:** on A11 devices (like the iPhone 8(+) or X) a variety of incompatibility problems may occur, like the breaking of the Touch/Face ID. try it at your own risk.

before starting, you also need to verify if the SEP of your iOS version (installed right now) is compatible with the version of iOS you want to dual boot. you can do this checking [this file](https://docs.google.com/spreadsheets/d/1Mb1UNm6g3yvdQD67M413GYSaJ4uoNhLgpkc7YKi3LBs/). finally, the last thing you have to verify is if you’re in a jailbreakkable version of iOS (the highest possible right now is the 14.8.1).

done all this, you’re ready to start! the first thing you have to do is…

## 1. JAILBREAK YOUR DEVICE
for this step, you need to install checkra1n on your mac, and you have to jailbreak your device. you can find checkra1n [here](https://checkra.in/).

## 2. DOWNLOAD AND SETUP DIVISÉ
Divisé is a powerful iOS tweak made by [MatthewPierson](https://github.com/MatthewPierson). it allows you to easily prepare your checkm8 vulnerable device to boot the second OS. download the tweak from the [Dynastic Repo](https://repo.dynastic.co/), open the new Divisé app appeared on your home screen, select the Dual boot option and then, after the explain, click on Download IPSW. you must select an iOS version compatible with your SEP (i know, it’s a big limitation). once you’ve done this, you need to attend the finish of the process (it may take some time), and at the end, click Back on the popup and after click on Dual boot device. give all the needed confirms, and when the process is done, you can finally proceed to boot the second OS! do not click reboot on the popup, but read directly the next step of the process.

**IMPORTANT:** remember what disk is indicated to you by the popup (ex *disk0s1s4*).

## 3. ENTER PWNDFU MODE
you have to put your device into a special DFU mode called PWNDFU mode. the process for this step is different for each chip, so i can only link you a github page (made by [nyuszika7h](https://github.com/nyuszika7h)) that contains all the methods (read only the step “Entering pwned DFU”, the rest is part of another tutorial). you can reach the page by clicking [here](https://gist.github.com/nyuszika7h/aac55c97f7925cddcf5ec3167f85dfe8).

## 4. DOWNLOAD ON YOUR MAC THE IPSW FILE
you must download on your mac the iPSW file for the iOS version you chose on Divisé. on [this page](https://ipsw.me/), select your device model and download the right file.

## 5. BOOT THE 2ND OS WITH RAMIEL
Ramiel is another tool made by [MatthewPierson](https://github.com/MatthewPierson) that you can [download here](https://ramiel.app/). Install it on your mac, open it, download all the necessary components and click on Advanced. select Boot Dualbooted OS, click on it and write the number of the disk that appeared on the Divisé popup before entering in PWNDFU mode. click now yes on each popup and now you can close the settings. you can finally click on Boot Device. click now on Run checkm8 and attend. this step is very critic for the process. in most cases, it will fail. if it happen, try again until it goes. Select now the iPSW file previously downloaded and wait for the process to finish.

if all went well, your device should have booted into the dual boot partition. have fun with your 2nd OS!

## VERY IMPORTANT!!
remember to not set a passcode at the 2nd OS!! it will break the booting of the partition. remember also to not erase the content of the 2nd OS from the settings.

**IMPORTANT:** when you will reboot your device, it will revert to the original iOS version. to boot again the 2nd OS, you have to re-jailbreak your device, open Divisé, click on Manage Dualboot, click on Mount the 2nd os, re-put your device in PWNDFU mode, re-open Ramiel and re-do the booting process.
