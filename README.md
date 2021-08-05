# 影音串流服務
`影音串流Streaming`跟一般靜態檔案加載最大的不同是串流可以逐塊加載並依據網速調整播放速度(adaptive bitrate streaming)

另外補充，`直播(Live Streaming)`和`影音串流(Vedio On Demand Streaming)`是類似但不同的串流領域，前者是由某影音錄製器如IP Camera/監視器/錄影機等即時錄影並將影像串流導向多個用戶 / 後者則是上傳靜態影片檔並經過處理，用戶觀賞影片並已串流方式分塊逐步下載而非完整檔案的技術。

### STREAMING PROTOCOLS
- HTTP:
  - 最廣泛使用的傳輸協定
- RTMP:
  - Real Time Messaging Protocol，由Adobe發起並支援於Flash中
- RTSP:
  - Real Time Streaming Protocol (RTSP)
### 影音串流格式
- MPEG-DASH:
  - Dynamic Adaptive Streaming over HTTP，透過W3C制訂的媒體源擴充功能Media Source Extensions(MCE)做串流，目前可由dash.js跨瀏覽器支援(IE11+)；
  - 可以透過XHR一塊塊下載檔案並串流至 html5影片播放元素上。
- HLS:
  - 由Apple發起並最先支援於iOS/Safari，現在Android/Chrome最新版也加入支援，瀏覽器可以透過 hls.js廣泛支援(IE 11+)
- Smooth Streaming：
  - 微軟制定的標準，檔案格式須為IIS Smooth Streaming。
- HDS:
  - HTTP Dynamic Streaming，由Adobe發起。
- 向下支援：
  - 可透過Flash播放器與RTMP傳輸協定。
---
### 架構圖
[wowza 範例](./pic/typical-streaming-workflow-1500x718.png)
