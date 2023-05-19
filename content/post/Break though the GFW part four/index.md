+++
author = "Wyane"
title = " 「翻牆」普及 Part Four - 應用部分 for iOS "
date = "2023-05-17"
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
lastmod="2023-05-19"

+++

## 前言

  對於移動端操作系統來說， iOS 上的工具可以說在**美觀**和**功能**上都勝過 Android 上的工具軟體。下面也是會介紹幾款**我使用過**的應用軟體。

## 軟體工具

### Shadowrocket

Shadowrocket 是一款兼容多種協議的網路工具，簡單易上手，許多的機場推薦工具中都會出現它的名字。當然也是我第一款接觸到的 iOS proxy 工具。

#### 購買方式

Shadowrocket 現在在除中國大陸區以外的 App Store 的主流區都有上架。目前美區價格是 $2.99

[商店地址](https://apps.apple.com/ca/app/shadowrocket/id932747118)

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

  項目地址：[Shadowrocket-ADBlock-Rules-Forever](https://github.com/Johnshall/Shadowrocket-ADBlock-Rules-Forever)

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

這是我目前主要使用的代理工具。個人覺得功能上比 shadowrocket 更加多元一些，也更加直接。對於一個代理工具來說，我覺得該有的功能基本都有了；但可能對於需要專業網路工具的用戶，surge 可能會是更好的選擇。

#### 購買方式

Quantumult X 現在在除中國大陸區以外的 App Store 的主流區都有上架。目前美區價格是 $7.99

[商店地址](https://apps.apple.com/us/app/quantumult-x/id1443988620)

#### 基本使用方法

* 添加訂閱

  1.  點擊右下角 `風車` 按鈕，在 `External Proxy` 中，點擊 `Resources`

  2.  複製你的 機場訂閱鏈接

  3.  將其粘貼到 `Resource URL` 中，`Tag` 欄是用來填寫名字的，你可以根據自己的喜好填寫

  4.  點擊左上角 `保存` 按鈕

     > 若出現 `Error` 的情況，可能是你的訂閱 Quantumult X 無法解析，需要先添加 `Recourse Parser` ，可先往下看，跳過添加訂閱這一步。

  5.  若添加成功，可以在主界面 `PROXY` 欄中看到你的訂閱節點，選擇節點後，點擊右上角的 `開關`，就可以正常使用了。

* 添加 Recourse Parser

  [Github 項目地址](https://github.com/KOP-XIAO/QuantumultX)

  1. 複製
  
     ```javascript
     resource_parser_url = https://raw.githubusercontent.com/KOP-XIAO/QuantumultX/master/Scripts/resource-parser.js
     ```
  
  2.  點擊右下角 `風車` 按鈕，下滑，點擊 `Edit`
  
  3. 在 `general` 中，粘貼上所複製的內容，點擊 右上角的 `✓` 
  
  4. 如果上一步中添加訂閱出現了問題，可以嘗試在添加訂閱時，將下面 Resource Parser 的開關按鈕開啓
  
     > 如提示"没有自定义解析器"，请长按 右下角 `風車` 按鈕后点击左侧刷新按钮，更新资源，后台退出 app，直到出现解析器说明
  
* 開啓 Rewirte 和 MitM
  
  * 安裝證書
  
    1.  點擊右下角 `風車` 按鈕，下滑，在 `MitM` 欄中，點擊 `Generate CA` 
    2.  點擊 `Install CA` ，選擇 `Download CA` ，跳轉到瀏覽器中下載證書
    3.  進入手機設置，在 `General` - `General` - `VPN & Device Management` ，找到並安裝相關的證書文件
    4.  再返回到 `General` ，點擊 `About` - `Certificate Trust Settings` ，開啓對於證書的完整信任
  
  * 打開 Rewrite 與 MitM 
  
    回到 Quantumult X ，點擊右下角 `風車` 按鈕，下滑，分別找到`Rewrite` 與  `MitM` ，開啓右邊開關
  
  
  
* GeoLite2
  
  [項目地址](https://github.com/P3TERX/GeoLite.mmdb)
  
  1. 複製地址: [長按複製](https://git.io/GeoLite2-Country.mmdb)
  
  2. 點擊右下角 `風車` 按鈕，下滑，在最下方點擊 `Misc Setting`
  
  3. 下滑，在 `GeoLite2` 右邊，點擊 `SOURCE` ，將剛剛複製的鏈接粘貼進去
  
  4. 點擊 `OK` ，再點擊 `Update`  
  
     
  
* 開啓 Proxy 
  
  1.  回到軟件的主界面，點擊右上角的開關按鈕
  2. 長按右下角 `風車` 按鈕，點擊 `三色風車` 圖標(Filter mode)
  
  > 關於三種顏色的風車，這裏做一下解釋
  >
  > 藍色風車 All Proxy mode :即全局代理模式
  >
  > 黃色風車 All Direct : 即全局直連模式 
  >
  > 彩色風車 Based on Filter : 規則模式，即你的網絡不會完全的被代理，會根據你自定的 Filter 和 Rewrite 進行變化
  >
  > 一般來說，我們更偏向於使用規則模式。因爲某些應用，我們並不想它被代理，或者，我們希望自定義代理它的路線，接下來會講到。
  
* Filter 添加
  
  推薦項目地址: [ios_rule_script](https://github.com/blackmatrix7/ios_rule_script)
  
  這裏我會儘量簡單的教會大家如何按自己的需求添加適合的 Filtter
  
  * 瞭解該項目
  
    點擊上面的項目鏈接，進入到項目頁面，可以看到下方有 `分流規則` 和 `複寫規則` 
  
    1. 點擊進入項目中 `分流規則` 下方提供的[鏈接](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule)
  
    2. 進入後，裏面按代理工具的不同而分成了幾個文件夾。我們選擇點擊 `QuantumultX` 文件夾
  
    3.  進入到這個目錄後，就又出現了更多的文件夾了。這裏文件夾的名字其實就是分流規則應用的名字了
  
        如果你需要哪一個應用的分流規則，就點進去使用就好了。
  
       > 具體的使用，下面會有一個例子。
  
  * 添加 Policy
  
    > 這裏以添加 [Instagram](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/QuantumultX/Instagram) 的分流規則作爲例子
  
    1.  回到 Quantumult X 中，在主界面中，`PROXY` 欄下方的右邊，有一個綠色的圖標，點擊它
  
    2.  進入後，在右上角 `✓` 的**左邊**，有一個類似於轉換的圖標，點擊一下
  
    3.  又進到了一個新的界面。因爲是給 instagram 的 policy ，所以可以 Policy Name 欄中輸入 instagram ， Icon 欄暫時我們還沒有設置圖標庫，可以待會再設置
  
       再往下，如果正常添加了訂閱節點的話，便可以看到下方有很多的節點。選擇幾個你想用的節點，點擊左邊的綠色圓形加號
  
       完成後點擊一下 右上角的 `✓` 
  
    這樣 ，一個給 instagram 的 Policy 就添加設置好了。
  
  * 添加 Filter 
  
    > 這裏以添加 [Instagram](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/QuantumultX/Instagram) 的分流規則作爲例子
  
    1. 回到第一步中的項目網頁(如果你關閉了，就先按照 瞭解該項目 的步驟，進入到應用分流目錄)，我們先找到 `Instagram` 的[文件夾](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/QuantumultX/Instagram)，然後點擊它
  
       > 這步可以用 **Command + F** / **Ctrl + F** ，後輸入 **Instagram** ，敲擊 `Enter` 就能更快的找到了 
  
    2. 進入後下滑，可以看到有很多種鏈接分支可以選擇，這裏就先使用 MASTER 分支 
       複製 MASTER 分支下方的[鏈接](https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/rule/QuantumultX/Instagram/Instagram.list) 
  
    3. 回到 Quantumult X 中，點擊右下角 `風車` 按鈕，在 Filter 板塊中，點擊 `Resources` 
  
    4. 點擊右上角(最右邊) 的圖標
  
    5. `Tag` 中可填 `instagram` 
  
    6. 將第2步中所複製的鏈接，粘貼到 `Resource URL` 欄中
    
    7. 打開 `Force Policy` 的開關，選擇到 instagram 的 Policy
    
    8. 點擊右上角的 `✓` 
    
       > 如果出現無法添加的問題，可以嘗試打開 `Resource Parser` 解決
    
    到這裏就已經大功告成了。回到主頁面，可以在 Policy 中爲 instagram 選擇使用一個特定的節點。這樣 instagram 的流量只會被你選擇的節點所代理。
    
    其實當體驗過這個功能，大概就能瞭解我爲什麼會把 Quantumult X  當成主力使用的其中一個原因。我之前有談到過流媒體的問題，就在於其實我也算半個流媒體中度用戶。主要有兩類，一類是各地區的內容會有所差異的流媒體，例如 Netflix 和 Disney+ 等；另一類就是鎖區型的。例如 peacock 和 Hbo 等等。有時候 Netflix 想要看的節目在港區，而 Disney+ 又想看臺區，這樣在換的i時候節點也要切來切去，實在是麻煩。更麻煩的i例如 peacock 這類需要美國地區節點，我平時又不會連在美國，就只能看的時候切到美國，不看的時候再把節點切回來。有夠麻煩真的。所以 Quantumult X  可以輕鬆的解決這個問題。只要爲特定的流量設置好 Policy，這樣你設置的軟體就會用特定的節點，而不是所有的軟體只被一個節點代理。這樣我在流媒體中切換的時候，就不需要將節點也進行切換了。
    
    
  
* Rewrite 添加
  
  * 添加方法
  
    1. 點擊右下角 `風車` 按鈕，下滑，找到 `Rewrite` ，點擊其中的 `Resource`
  
    2. 一般我們都是通過鏈接導入的。這裏僅說明通過鏈接導入的方式。
  
       點擊右上角(最右邊) 的圖標
  
    3. `Tag` 中填入給 Rewrite 取的的名字
  
    4. 將所複製的鏈接，粘貼到 `Resource URL` 欄中
  
    5. 打開 `Resource Parser` 的開關
  
    6. 點擊右上角的 `✓` 
  
  * Rewrite 可以拿來做什麼
  
    Rewrite 就是指對一些網絡流量進行重寫。可以通過這個功能，爲一些 app 去廣告，或者應用重寫等的實現。
  
    [Sub-Store](https://www.notion.so/Sub-Store-6259586994d34c11a4ced5c406264b46) 和 [boxjs](https://docs.boxjs.app/) 都可以通過 Rewrite 進行安裝，兩款非常有用的工具。
  
    推薦項目：[ddgksf2013](https://github.com/ddgksf2013/ddgksf2013) 有許多有用的 Rewrite 在這個項目中能找到
  
  

  

  

  

  

  

