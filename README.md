# SJB.booking.com

SJB.booking.com 是一個旅遊訂房網站

## 專案特色

分為前、後台兩個不同的⽤戶界⾯：前台針對旅客提供註冊、查詢飯店、房間、下訂單及加⼊購物⾞等功能，⽽後台則針對業者提供管理飯店、房間和訂單的功能。
使⽤JavaMail提供註冊及下訂單後發送email通知功能。
提供購物⾞功能，將多筆房間累積後以Pinia將資訊送至結帳⾴⾯，⼀次性下訂單。
提供Google第三方登⼊，並串接綠界科技API做為第三方結帳金流。
使⽤WebSocket提供旅客與業者的聊天通訊功能。

### 後端功能
統一使用RESTful風格來製作並拆分MVC提升維護性以及降低代碼間的耦合度，為防止Null Pointer的發生，運用了`Optional` 來判斷空值，Json序列化時所發生的異常透過@`JsonIgnore` 防止，安全性上使用bcrypt加密為會員的資料提升安全性。
### 前端功能
ajax非同步請求則使用了axios庫來達成並在多處使用了ES8引入的async await來提昇代碼的清晰度，樣式則是使用了bootstrap5、原生CSS以及SweetAlert2來製作清晰明亮的畫面。
