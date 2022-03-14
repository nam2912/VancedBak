# VancedBak
A backup of all apk files for both Vanced Youtube and Music with (most) of it versions in this repo.

# How to download?
WIP

# How to Install?
### SAI Method (Rooted & NonRooted)
1.) Uninstall YouTube through settings or through Google Play Store (why? who uses play store to uninstall shit 💀) \
2.) Install ZARChiver and SAI (Split APK Installer) in the Google Play Sore. \
3.) With the downloaded zip of Vanced, extract the zip to a place where you're most likely to remember (I use /sdcard/Documents/Vanced) \
4.) Once extracted go to SAI go to settigns then disable `Sign APKs` \
5.) Go back to the Installer tab and press the Install APK's and use Internal File Picker then go to the folder where you extracted it and choose which folder to use if you are rooted or not. \
We would need to pick 4 apk files:
- `base.apk`
- `dpi.apk`
- `split_config.arm64_v8a.apk` (For ARM64 CPU's only (most phones use ARM cpu's), to check you're CPU Architecture install Termux and type in `getprop ro.product.cpu.abi` and it should show your CPU Architecture for you to use.)
- `split_config.en.apk` (You can change this to whatever language you wan't within the Language folder)

If done correctly step by step, you should be able to have Vanced installed onto you're phone!

### Terminal Method (for Rooted)
1.) Uninstall YouTube through settings or through Google Play Store \
2.) Install ZARChiver and SAI (Split APK Installer) in the Google Play Sore. \
3.) With the downloaded zip of Vanced, extract the zip to a place where you're most likely to remember (I use /sdcard/Documents/Vanced) \
4.) Once extracted go to SAI go to settigns then disable `Sign APKs` \
5.) Go back to the Installer tab and press the Install APK's and use Internal File Picker then go to the folder where you extracted it and choose which folder to use if you are rooted or not. \
We would need to pick 4 apk files:
- `stock.apk` (MAKE SURE ITS STOCK)
- `dpi.apk`
- `split_config.arm64_v8a.apk` (For ARM64 CPU's only (most phones use ARM cpu's), to check you're CPU Architecture install Termux and type in `getprop ro.product.cpu.abi` and it should show your CPU Architecture for you to use.)
- `split_config.en.apk` (You can change this to whatever language you wan't within the Language folder)

If done correctly step by step, you should be able to have the stock YouTube app installed for Vanced to be installed to. \

6.) Install and open up Termux and `su` and it should ask for Root Permission, press Grant on the popup.
7.) Type in `pm path com.google.android.youtube` and it should pop out with 4 packages.
8.) Long press the screen to select the text and select the directory **WITHOUT** the apk inside it, then press Copy.
9.) Type in `cd /path/to/vanced/root/Theme`, to check if you are in the directory type in `ls` and check if the dark, black, dpi, stock apks.
10.) Pick out you're preffered theme, type in `mv ./(ur theme apk).apk ./base.apk`, and type in `ls` and check if you're apk got renamed to `base.apk`
11.) Type in `cp ./base.apk (long press the screen and press paste to add the path)`. (Check the screenshot below)
12.) To check we have changed the apk successfully, type in `diff ./base.apk (long press the screen and press paste to add the path)`, and if nothing came out, move onto the next step.
13.) Type in `chcon -R u:object_r:system_file:s0 (paste in directory)/base.apk`, and if it didnt spit out errors go to the next step.
14.) Go to Settings > Apps > See all apps > YouTube
15.) Press Force Stop and then open the app.

If done correctly step by step, you should be able to have Vanced installed onto you're phone!
