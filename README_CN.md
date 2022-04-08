# StreetFighterDuel_Tools: “街霸：对决”逆向及解密工具 

[English Version](README.md)

[TOC]

- [x] [解包](#unpack)
- [x] [逆向](#Reverse)
- [x] [解密](#decrypt)
- [ ] [打包](#repack)




## 解包 <span id="unpack">

- **提示**:   
  - 首先下载游戏包apk, 可以试试[app.mi.com](https://app.mi.com/details?id=com.tencent.vega&ref=search)/[gamedog](http://www.gamedog.cn/online/2711920/)/[taptap.io](https://taptap.io), 等等
  - 解压缩可以使用7zip/apktoolbox
  - 反编译/编译DEX, 使用apktool等
  - 反编译jar到java, 使用dex2jar, jd-gui或者cfr.
- **Windows**:  
  - 使用Explorer资源管理器/7zip/unzip/apktoolbox 解压缩apk
  - 使用apktoolbox等反编译DEX
- **linux/macOS**:
    ```
    $ unzip (StreetFighterDuel).apk
    ```

## 逆向 <span id="Reverse">
- **提示**: 
  - 需要一个ROOT过的设备或者模拟器（目前模拟器暂不支持解密）
- **工具**:
  - [FrIDA](https://frida.re)/[objection](https://pypi.org/search/?q=objection)/[Python 3](https://www.python.org/)/[vscode](https://code.visualstudio.com/)/[node.js](https://nodejs.org/en/)/[IDA 7.x(optional)](https://hex-rays.com/)/[vs2019/2022](https://visualstudio.microsoft.com/)/[android studio(sdk)](https://developer.android.google.cn/), 等等
  - 个人喜好vb6, 别恨我
- **Windows**:
  - 已ROOT过的设备:
    - 安装 (StreetFighterDuel).apk到设备
    ```
    > adb install (StreetFighterDuel).apk 
    ```
    - 安装本工具自带decryptSFD.apk到设备
    ```
    > adb install decryptSFD.apk 
    ```
    - 打开 "Developer Command Prompt for VS 2019"命令行工具
    - 运行设备上的“街霸：对决”，登录并自动下载更新文件
    ```    
    > frida -U -f com.tencent.vega --no-pause
    ```    
    - 运行工具自带批处理工具复制所有相关文件到本地
    ```    
    > start copySFD.bat
    ```
    - 使用Frida/IDA/objection寻找Sqlite/XXTEA密码, 不是很容易，祝好运！
    <!-- > start powershell -command "objection  -g com.tencent.vega explore" -->
    ```    
    > frida -U -f com.tencent.vega -l getkey.js --no-pause
    ```
  - 已ROOT过的模拟器:    
    - 暂不支持，尚未实现x86/x86_64平台支持。
- **linux/macOS**:
  - 暂不支持。
## 解密 <span id="decrypt">
Chunli:

<a href="https://github.com/ipengci/StreetFighterDuel_Tools"><img src="images/chunli.gif" width = "100%" height = "100%" alt="图片名称" align=center /></a>

Cammy:
<a href="https://github.com/ipengci/StreetFighterDuel_Tools"><img src="images/cammy.gif" width = "100%" height = "100%" alt="图片名称" align=center /></a>

## 打包 <span id="repack">
- 暂不支持打包，尚未实现。

## 注意 <span id="note">
本工具仍在开发中，进展较慢，错误难免，尚未稳定，敬请原谅!
请发 [e-mail](mailto:326812493@139.com) 到 [326812493@139.com](mailto:326812493@139.com)了解动态和获取方法。

为加快研发进度，请考虑捐助，谢谢！

支付宝：

<a href="https://github.com/ipengci/StreetFighterDuel_Tools"><img src="images/alipay.png" width = "200" height = "255" alt="图片名称" align=center /></a>

微信：

<a href="https://github.com/ipengci/StreetFighterDuel_Tools"><img src="images/wechat.png" width = "200" height = "247" alt="图片名称" align=center /></a>

