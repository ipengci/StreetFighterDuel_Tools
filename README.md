# StreetFighterDuel_Tools

Tools to reverse engineer, decrypt StreetFighter Duel, the mobile game by [Topjoy](https://topjoy.com) .
<!-- and [Tencent](https://game.qq.com). -->

[中文版](README_CN.md)

[TOC]

- [X] [Unpacking](#unpack)
- [X] [Reverse Engineering](#Reverse)
- [X] [Decryption](#decrypt)
- [ ] [Repacking](#repack)



## Unpacking <span id="unpack">

- **Tips**:   
  - To get the game's apk, try [app.mi.com](https://app.mi.com/details?id=com.tencent.vega&ref=search)/[gamedog](http://www.gamedog.cn/online/2711920/)/[taptap.io](https://taptap.io), etc.
  - To unpack the apk, use 7zip, etc.
  - To de/recompile the DEX, use apktool
  - To decompile jar to java, use dex2jar, jd-gui/cfr.
- **Windows**:  
  - Use Explorer/7zip/unzip/apktoolbox to unzip the apk
  - Use apktool to decompile to smali
- **linux/macOS**:
    ```
    $ unzip (StreetFighterDuel).apk
    ```

## Reverse Engineering <span id="Reverse">
- **Tips**: 
  - A rooted android driven device/emulator   
- **Tools**:
  - [FrIDA](https://frida.re)/[objection](https://pypi.org/search/?q=objection)/[Python 3](https://www.python.org/)/[vscode](https://code.visualstudio.com/)/[node.js](https://nodejs.org/en/)/[IDA 7.x(optional)](https://hex-rays.com/)/[vs2019/2022](https://visualstudio.microsoft.com/)/[android studio(sdk)](https://developer.android.google.cn/), etc.
  - I prefer vb6, don't hate me.
- **Windows**:
  - For rooted devices:
    - Install (StreetFighterDuel).apk to device
    ```
    > adb install (StreetFighterDuel).apk 
    ```
    - Install decryptSFD.apk to device using adb install
    ```
    > adb install decryptSFD.apk 
    ```
    - Open "Developer Command Prompt for VS 2019"
    - Run StreetFighter Duel and let it download updates
    ```    
    > frida -U -f com.tencent.vega --no-pause
    ```    
    - Then copy all updated data
    ```    
    > start copySFD.bat
    ```
    - Use Frida/IDA/objection to find Sqlite/XXTEA keys, not easy, good luck!
    <!-- > start powershell -command "objection  -g com.tencent.vega explore" -->
    ```    
    > frida -U -f com.tencent.vega -l getkey.js --no-pause
    ```
  - For rooted emulator:    
    - Not yet working because the x86/x86_64 port not implemented.
- **linux/macOS**:
  - NOT yet implemented, maybe never.
## Decryption <span id="decrypt">
Chunli:

<a href="https://github.com/ipengci/StreetFighterDuel_Tools"><img src="images/chunli.gif" width = "100%" height = "100%" alt="图片名称" align=center /></a>

Cammy:
<a href="https://github.com/ipengci/StreetFighterDuel_Tools"><img src="images/cammy.gif" width = "100%" height = "100%" alt="图片名称" align=center /></a>

## Repacking <span id="repack">
- Repacking is not yet implemented, maybe never.

# Note: <span id="note">
This is in progressing, sorry for the delay!
Please send [e-mail](mailto:326812493@139.com) to [326812493@139.com](mailto:326812493@139.com) to get the tools by now.

Please consider donate to keep this available, thanks a lot!

Paypal: [https://paypal.me/bihaiorg](https://paypal.me/bihaiorg)
<!-- ![paypal](images/paypal.png "https://paypal.me/bihaiorg" ) -->
<a href="https://paypal.me/bihaiorg"><img src="images/paypal.png" width = "200" height = "200" alt="图片名称" align=center /></a>

<!-- 
Alipay: 

<a href="https://github.com/ipengci/StreetFighterDuel_Tools"><img src="images/alipay.png" width = "200" height = "255" alt="图片名称" align=center /></a>

Wechat: 

<a href="https://github.com/ipengci/StreetFighterDuel_Tools"><img src="images/wechat.png" width = "200" height = "247" alt="图片名称" align=center /></a>

 -->
