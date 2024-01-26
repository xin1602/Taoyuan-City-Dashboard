#   Taiyuan City Dashboard 桃園城市儀表板
## 主題：讓我們不再「行」同「默」路

### 1. 本戰情中心希望解決的智慧城市問題
在2021年，臺灣的交通問題引起國際關注，更被國際媒體稱為「行人地獄」。政府回應這一問題的政策之一是推動行人專用時相。因為行人專用時相將人流及車流分開，不僅僅可以降低事故率，還可以讓右轉車不需要等待行人通行，確保交通效率。然而，截至2023年，身為六都之一的桃園市行人專用時相數量仍然偏低。為了改變這一現象，我們提出了一個智慧城市解決方案，致力於提升交通安全性並優化交通流動。
### 2. 解決方式
解決方式旨在改善智慧城市中的行人安全問題與交通問題，特別針對行人專用時相的設置地點、開啟時段與秒數調整。我們透過預測、處理與績效三大子系統的整合來提高交通效能和行人安全性，並將數據分析視覺化，以優化決策者的使用體驗與效率。

#### 2.1. 層級式儀表板
允許決策者在總體上查看所有路口的總體概要數據[路口管控]；同時也提供深入到單一路口[中北路口]的能力，以便進一步分析和了解細節。
#### 2.2. 行人專用時相設置與時段
透過儀表板中的［人流量］和［壅塞路段(車流)］因素判斷是否需要在特定路口與特定時間設置行人專用時相。考慮到 [道路寬度]，我們確保行人能夠安全穿越。根據桃園市政府資料開放平台與施政方針、我們在中原大學周遭的親身觀察、儀表板提供的數據、各項新聞內容等等，我們選擇實作在［中北路、實踐路口］進行行人專用時相的路口範例。
#### 2.3. 紅綠燈秒數調整
為確保車輛和行人之間的交通協調，我們透過數據分析和設置來調整紅綠燈時間。而行人專用時相最主要的服務對象為「行人」，因此我們將會以 [人流量] 數據為主，其餘為輔作為設置紅綠燈秒數的基準。
#### 2.4. 績效評估
安裝行人專用時相後，我們持續監測 [中北路口] 的績效。這包括人車事故的減少、交通效能的改善和派警次數的降低。如果路口的績效指標在設置行人專用時相後有明顯改善，則代表我們的解決方案取得成功。

### 3. 三大模組
解決方案包含三個子系統：績效子系統、預測子系統、處理子系統。
#### (1).績效子系統
此子系統針對交通局的公務人員，根據以下三項計算指標權重來評估行人專用時相的效果。
<br />
1.1.人車事故（40%）：人命，是我們最重視的部分，也是被冠上行人地域的主要原因之一。如果人、車分流的行人專用號誌是有效的，那就可以預期車禍數量可以降低，尤其是行人與車輛之間的車禍。
<br />
<br />
1.2.交通效能（30%）：考慮到行人專用時相設置後紅綠燈秒數的調整，我們需評估此改變是否會使交通更加順暢，或反而導致更嚴重的壅塞情況。因此我們重要的是分析人、車分流對交通流動的影響，以確保車輛能夠順利通行，避免因行人穿越馬路而導致的交通回堵。根據以上因素分析，我們採用統計量化指標：人車平均停等時間來作比較。

    人車平均停等時間=所有通行行人通行車輛的總停等時間/通行路口的行人車輛的總數
<br />
1.3 派警次數（30%）：過去在人、車流量龐大的路口經常需要交通警察進行指揮與疏散。裝設行人專用時相後，我們期望能夠降低派遣警力的頻率，從而提升路口的績效。相反地，若裝設行人專用號誌後需要更多警力協助交通指揮，該路口的績效則會下降。這項指標的目的在於反映系統在警力利用效率方面的影響。
<br />

#### (2).預測子系統
我們設計了預測子系統，利用歷史人流量、車流量以及路段壅塞資料，預測需要裝設行人專用時相的路口、合適的啟用時段與紅綠燈秒數的設置時間。
<br />
2.1. 根據 [人流量]、[車流量]的歷史資料，以及 [各個路段的壅塞資料] 預測哪個路口需不需要裝設行人專用時相，以及裝設之後要在甚麼時間開啟 。
<br />
根據 [人流量] 歷史資料，加上 [道路寬度] 、 [路口人流承載量] 等已知資料，預測行人的紅綠燈時間以及車子的紅綠燈時間。本系統秒數設定情境描述：我們透過數據知道，路口15分鐘會累積的人流量高達900人，於是可知10秒鐘就大約累積10個人。假設此路口人流承載量上限是100人，累積到100人的時候，就必須讓行人疏散，此時行人就必須綠燈。那行人在綠燈前的紅燈100秒，也就會是車子的綠燈時間。而因為是十字路口，有兩道的車流，100秒還需要除以2，這樣我們就得到車子的綠燈秒數50秒了！此設計方式是為了最大化的讓人流通過，在疏散人和疏散車之間取得平衡。
<br />

#### (3).處理子系統
處理子系統則根據預測數據有效地裝設行人專用時相，並精確計算綠燈時間，以最大程度地利用路口資源，並為兩種不同的情況建制處理子系統：
<br />
3.1.	有效疏散
<br />
3.1.1.	開啟時段：根據預測數據鎖定行人專用時相目標安裝路口，並透過各時段人流量決定開啟時段。
<br />
3.1.2.	調整秒數：在此目標路口調整紅綠燈秒數並建設警示牌告知用路人，避免用路人認為是號誌故障而導致成效不彰。
<br />
3.2.	無效疏散
<br />
3.2.1.	績效評估：觀察績效子系統的量化指標，若發現分數有不增反減的趨勢，意即發生例外狀況，須由公務員親自因地制宜調整合適的配置時間。
<br />


#### (4).系統呈現
<img src='src/assets/images/dashboard_intersection.png'> 
<img src='src/assets/images/dashboard_zhongbei_intersection.png'> 
<img src='src/assets/images/map01.png'> 
<img src='src/assets/images/map02.png'> 
<img src='src/assets/images/map03.png'> 
<img src='src/assets/images/map04.png'> 
<img src='src/assets/images/component_detail.png'> 



## Quick Start

### Docker

1. Install [Docker](https://www.docker.com/products/docker-desktop/) on your computer and start running it.
2. Fork this repository then clone the project to your computer. Execute `pwd` (mac) or `cd` in the repository terminal to get the complete path.
3. Execute the following command in the system terminal and replace "<repository path>" with the path you got in step 2.

```bash
docker run -v <repository path>:/opt/Taipei-City-Dashboard-FE -p 80:80 -it node:18.18.1-alpine3.18  sh
```

4. Execute the following commands to enter the project folder and install packages.

```bash
cd /opt/Taipei-City-Dashboard-FE
npm install
```

5. You should now be able to locally host this project by executing `npm run dev` in the respository terminal.
6. Refer to the [Docs](https://tuic.gov.taipei/documentation/front-end/project-setup) to complete further configurations.

### Local Environment

1. Download [Node.js](https://nodejs.org/en) on your computer.
2. Fork this repository then clone the project to your computer.
3. Execute `npm install` in the respository terminal
4. You should now be able to locally host this project by executing `npm run dev` in the respository terminal.
5. Refer to the [Docs](https://tuic.gov.taipei/documentation/front-end/project-setup) to complete further configurations.

## Documentation
Develop Taoyuan City Dashboard based on Taipei City Dashboard.
Check out the complete documentation for Taipei City Dashboard FE [here](https://tuic.gov.taipei/documentation).
