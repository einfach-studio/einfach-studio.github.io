---
title: "談談工作流程"
cover: "https://www.calmachiever.com/wp-content/uploads/2017/03/Supercharge.jpg"
date: "2017/09/09"
category: "talks"
tags: 
    - 專案管理
    - 時間管理
---


最近DB為了要讓自己工作更有效率，希望用最短的時間把任務一次做完~~然後準時下班~~，開始嘗試應用一些工作方法。試用以後，有一些不同的心得想分享。

我們先一步步來，認識一下有哪些「有效率」的工作方法。

## 有效率的工作方法
工作方法有很多種，大原則不外乎以下幾點：

1. 一眼就能看懂的明確目標
2. 計算花費時間，限時 or 計時
3. 區分任務優先順序
4. 了解自己的能耐，不貪多

以下就簡單介紹我聽過的方法。

### pomodoro 番茄鐘

* 每30分鐘為一單位的蕃茄鐘，25分鐘工作、5分鐘休息
* 每6個蕃茄鐘安排一次長時間休息
* 任務切割成小單位，以「幾個蕃茄鐘」的方式安排日程

每個人可專注的時間不一定，但普遍都不會超過90分鐘。因此，將任務切割成小單位，以蕃茄鐘為單位短期衝刺，把困難的任務用「每次做一點」的方式做完。

其實可依自己習慣修改作法。以我來說專注30分鐘真的太短了，所以改成每1小時為單位去排。

重點就是：切成小目標、定時、做一段時間要休息

### GTD (Getting Things Done)

1.  建立收集夾放「任何關於專案、工作的一切」（任務、目標、困惑、資訊....）
2. 分類（按內容、流程階段...）
3. 拆成具體待辦事項
3. 按輕重緩急排順序
4. 一次只專心做一件事
5.  定期清空收集夾

**「Think One & Do One」**。GTD包含了幾個核心概念：

* 收集 -> 規劃 -> 專心做一件事
* 寫下來，不要用腦袋記
* 唯一的收集夾，要定期清空

GTD簡化了可能讓腦袋混亂的流程，因為**腦袋是用來思考、它的可靠性是不被信任的**。經常會搭配使用待辦清單（To Do List）、或者Trello等其他工作方法、工具實現。

### The 1-3-5 Rule

* 每日清單這樣列
	* 1件重要任務（3h）
	* 3件中型任務（1件1h）
	* 5件瑣事（1件30min）
* 瑣事下班前再處理
* 任務要非常明確
* 盡可能不要列滿這張清單

我們都知道可以列待辦清單，但經常因為清單太長做不完、任務又寫得不具體看不懂在幹麻。那怎麼列才算有效？

**「只列做得完的清單」**，一天就列這幾件事，**最好還不要列滿**，以便能應付臨時的插件。


### Time Tracking

* 使用計時器追蹤每件任務花費時間
* 根據結果做調整

實際作法很簡單，開始每個任務時，按下計時器、碼表，中途短暫離開按暫停、任務結束時按停止。

這個很適合SOHO族精算自己的實際工時，方便做規劃、報價。

### 參考來源

想知道詳細的實作步驟、相關的工具，請參考[電腦玩物](http://www.playpcesor.com/)的文章，基本上這些全都是從那邊學來的，包含筆記的方法也是，對這方面有興趣的歡迎關注[電腦玩物](http://www.playpcesor.com/)喔！

----------

## 反思

看完了，然後呢？
接下來的部份，我要說說自己試用後的心得。

### 適合自己就是好方法

工作方法這麼多，到底哪種好用？

__適合自己的方法最好用。__

~~這不是在講幹話，~~那要怎麼挑呢？

回歸到自己的需求，覺得自己在浪費時間就用Time Tracking工具、覺得不知道該做什麼，就用GTD和1-3-5法則。總之，__親自試過立刻就會知道適不適合__。違反自己性格、習慣的事肯定沒辦法長久，這個只能自己嘗試、自己歸納哪種好用。

### 規劃其實很浪費時間

我用了Time Tracking工具追蹤這個月的工作狀況時，發現了一個有趣的現象：每天一早的「規劃」其實花了我最多的時間。這點其實很弔詭，良好的規劃可以省下時間、但規劃時間又很浪費時間。

### 剖析痛點，節省規劃時間

仔細探究後，我發現問題出在以下幾點：

1. 規劃資料分散在各服務中
2. 工具很難操作
3. 花太多時間做筆記

甚至有一天花了2小時就為了把hackMD的筆記改寫格式到Trac中回報進度，根本超浪費時間的我說。

身為小工程師，決定要優化這個流程。

首先是架構好自己的工作流程：每天一來我要怎麼開工？用什麼服務看進度？用什麼工具追蹤狀況？回報進度時要用到哪些工具？怎樣的流程最順手？

以我自己來說，我用了以下工具：

* 專案管理：Trello
* 筆記、草稿、規劃：hackMD
* 進度回報：Trac
* 時間追蹤：Toggl
* 每日待辦事項：Todoist

因為太分散，資料搜尋、同步的成本很高，所以我決定使用基於API和webhook的自動化服務，把我愛用的服務們串接在一起。好比說：Trello在卡片中新增待辦事項時，自動在Todoist新增一個Task、hackMD透過格式轉換工具轉成Trac的格式...等。下次再另開一篇介紹我的wrokflow和自動化工具zapier怎麼使用。

## 小結

今天簡單介紹了工作方法&一些心得，利用這些方法可以多多認識自己，越了解自己的習性、就能工作越有效率，~~然後準時下班走人！~~