+++
author = "Wyane"
title = " 「翻牆」普及 Part Four - 應用部分 for iOS "
date = "2022-04-05"
description = ""
tags = [
    "Technology",
    "GFW",
    "iOS",
]
categories = [
    "Technology",
]
series = ["Themes Guide"]
aliases = ["migrate-from-jekyl"]
image = "background.png"

+++

## 前言

  對於移動端操作系統來說， iOS 上的工具可以說在**美觀**和**功能**上都完勝 Android 上的工具軟體。這也是我習慣使用 iOS 進行「翻牆」操作的原因之一。下面也是會介紹幾款**我使用過**的，也是比較主流的應用軟體。

## 軟體工具

### Shadowrocket

Shadowrocket 是一款兼容多種協議的網路工具，簡單易上手，包括穩定，許多的機場推薦工具中都會出現它的名字。並且由於存在多年，相信許多人對它也有着一定的感情，隨着幾年的更新，功能也越來越完善。

#### 購買方式

Shadowrocket 現在在除中國大陸區以外的 App Store 的主流區都有上架。目前美區價格是 $2.99。

#### 基本使用方法

* 添加訂閱 / Add Subscribe

  1.  點擊 右上角 `+` ，再點擊 `Type` ，在選項中點擊選擇 `Subscribe` 

  2.  複製你的 機場訂閱鏈接

  3.  將其粘貼到 `URL` 欄中，點擊右上角的 `Done` 

     > 可以在 `Remarks` 欄中，備註自己的訂閱。相當於給自己的訂閱取名字，在你有多個訂閱鏈接時就容易區分了。

  4.  等其下載完成後，就在主界面就可以看到剛剛添加的訂閱了。在訂閱中選擇一個節點， 打開 `Not Connect` 旁的開關，就可以使用了。

* 添加節點

  Shadowrocket 添加單個節點的方式有很多，但因爲現在大部分機場都直接提供了訂閱鏈接，所以具體就不做過多介紹了。

#### 進階功能配置

首先我們需要瞭解 Shadowrocket 的**四種**路由配置(Global Routing)

在 `Home` 界面中，點擊 `Global Routing` ，就可以看到他提供的幾種方法。

* 配置 / Config

  選用配置規則的方法來進行鏈接。點擊**底欄中的第二個選項**  `Config` ，在 `Local Files` 就可以看到你現在選中的配置文件。Shadowrocket 會有一個自帶的配置(default.conf)。你也可以添加自己的配置，使網路連接在自己定製的「規則」範圍內進行。例如分流（例如國內IP直連，國外網站自動走代理），通過 HTTPS解密 實現去除廣告等的功能。

* 代理 / Proxy

  默認全局代理。簡單來說你手機上的所有流量被代理。可能有一些不需要代理的軟體也會被代理。

* 直連 / Direct

  不通過代理，直接訪問網路。 簡單來說就是你的所有流量都不會被代理。

* 場景 / Scene

  Shadowrocket 的場景功能是可以通過你當前所連接的Wi-Fi或移動網路來切換節點或關閉代理。

以上四種路由配置，我們最基本的也就是使用**配置 / Config**這種方式，所以就先來講講如何更改配置並實現 HTTPS解密。

* 配置 / Config

  對於一般使用者來說，要自己寫配置文件有點困難。所以我們可以使用 Github 上別人開源的一些項目，導入別人寫好的配置。

  項目地址：[Shadowrocket-ADBlock-Rules](https://github.com/h2y/Shadowrocket-ADBlock-Rules)

  1.  先在項目中，找到一個適合你的分流規則，並複製他的規則地址
  2.  打開 Shadowrocket，點擊底欄中的 `Config` ，點擊 右上角 `+` ，把剛剛複製的規則地址粘貼到裏面，點擊 `Download`  
  3.  完成後，就可以看到下方 `Remote Files` 有了一個配置文件，點擊它，再選擇 `Use Config` 
  4.  成功後，`Local Files` 看到新的配置文件，再點擊新加入的配置文件，選擇 `Use Config` 
  5.  點擊配置文件右邊的 `！` ，點擊 `HTTPS Decryption` ，點擊右上角的開關，會彈出證書的安裝
  6.  點擊 `install CA Certificate to System` ，會跳轉到 Safari 下載證書文件
  7.  等待下載完成後，到手機 `Settings` - `General` - `VPN & Device Management` ，安裝關於 Shadowrocket 的文件
  8.  再返回到 `General` ，點擊 `About` - `Certificate Trust Settings` ，開啓對於 Shadowrocket 證書的完整信任
  9.  打開開關後，回到 Shadowrockt ，繼續在剛剛的 `Certificate` ，點擊右上角的開關

  完成以上步驟後，就已經完成配置功能了。

### Quantumult X

功能上比 Shadowrocket 更加多元的網路工具，並且具有極高的自定義性，相比於 Surge，性價比也高出不少，並且界面也做的很好看。

#### 購買方式

Quantumult X 現在在除中國大陸區以外的 App Store 的主流區都有上架。目前美區價格是 $7.99。

#### 基本使用方法

* 添加訂閱

  1.  點擊右下角 `風車` 按鈕，在 `External Proxy` 中，點擊 `Link`

  2.  複製你的 機場訂閱鏈接

  3.  將其粘貼到 `Resource URL` 中，`Tag` 欄是用來填寫名字的，你可以根據自己的喜好填寫

  4.  點擊左上角 `保存` 按鈕

     > 若出現 `Error` 的情況，可能是你的訂閱 Quantumult X 無法解析，需要先添加 `Recourse Parser` ，可先往下看，跳過添加訂閱這一步。

  5.  若添加成功，可以在主界面 `PROXY` 欄中看到你的訂閱節點，選擇節點後，點擊右上角的 `開關`，就可以正常使用了。

* 添加 Recourse Parser

  [Github 項目地址](https://github.com/KOP-XIAO/QuantumultX)

  1.   先點擊上方的項目地址，複製裏面的 `Quantumult X 资源解析器` 鏈接
  2.  

  

  

  

  

  

