# 💎 Jewelry Store Ordering System
> 一個以 **Java Swing + MySQL** 打造的桌面版珠寶購物系統  
> 提供會員登入、下單、折扣計算、庫存更新與訂單查詢功能。  

---

## 🧭 專案簡介
本系統模擬實體珠寶店的銷售流程，從會員登入、商品選購、訂單確認、折扣計算到庫存扣減，  
完整呈現 **MVC 架構的桌面應用開發流程**。  

本專案以物件導向思維進行分層設計，適合作為 **Java 應用程式架構範例** 及 **面試作品展示**。

---

## 🛠️ 技術架構
| 分層 | 功能說明 | 實作技術 |
|------|----------|----------|
| UI 層 | 使用者操作介面（下單、確認、發票、登入） | Java Swing / JFrame / JTable |
| Service 層 | 業務邏輯（折扣判斷、首購優惠、資料整合） | 自訂 Service + Interface |
| DAO 層 | 資料庫操作（查詢、更新、刪除、庫存扣除） | JDBC / MySQL |
| Model 層 | 資料模型封裝 | Java Bean (POJO) |
| Util 層 | 工具（資料庫連線、物件序列化、共用函式） | File I/O / JDBC 連線管理 |

---

## 🧩 功能特色
- 👤 **會員系統**：登入驗證、首購判斷、自動折扣計算  
- 💍 **商品下單**：可選擇戒指、耳環、項鍊、手環等商品  
- 💸 **自動折扣**：會員等級折扣 + 首購 95 折  
- 🧾 **訂單列印**：支援訂單明細列印 (JTable → 印表機)  
- 🏬 **庫存管理**：下單自動扣庫存、庫存不足警示  
- 💾 **CRUD**：使用 MySQL + Java 序列化保存暫存資料  

---

## 📁 專案結構
src/
├─ controller/ # UI 控制邏輯 (AddOrderUI, ConfirmUI, FinishedUI)
├─ dao/ # 資料庫存取層 (ProductDAOImpl, JewelryOrderDaoImpl)
├─ model/ # Java Bean 模型 (Customer, JewelryOrder)
├─ service/ # 業務邏輯介面與實作
│ ├─ customer/impl/CustomerServiceImpl.java
│ └─ impl/JewelryOrderServiceImpl.java
├─ util/ # 工具類 (Tool.java, TableModel)
└─ resources/ # 圖片與測試素材

---

## ⚙️ 開發環境
- Java 11  
- Eclipse / windowbuilder  
- MySQL 8.0.33  
- JDBC Driver 8.x  
- OS：Windows / macOS 均可執行  

---

## 🚀 專案執行方式
1. 匯入專案到 Eclipse 
2. 修改 `Tool.java` 裡的資料庫設定：
   String url = "jdbc:mysql://localhost:3306/jewelryorder";
   String user = "root";
   String password = "1234";
3. 執行 controller.LoginUI進入系統
4.測試消費者帳號:cus1  密碼:123
  測試管理員帳號:admin 密碼:admin
5.測試下單流程，確認折扣、庫存與發票功能

🧠 Design Highlights | 系統設計重點

🔹 採用 MVC 架構：確保前端與業務邏輯分離，易於維護

🔹 應用 OOP 封裝與繼承：每個功能模組清晰獨立

🔹 JDBC + DAO 模式：資料庫操作結構化

🔹 Swing GUI 整合：自訂樣式、色彩與事件控制

🔹 檔案暫存機制：序列化保存暫時登入與訂單資料

📸 Screenshots | 系統畫面
畫面	預覽

登入畫面	
![LoginUI](UI/LoginUI.png?raw=true)<br>

登入成功畫面
![LoginSuccessUI](UI/LoginSuccessUI.png?raw=true)

登入失敗畫面
![LoginErrorUI](UI/LoginErrorUI.png?raw=true)

會員註冊畫面
![AddCustomerUI](UI/AddCustomerUI.png?raw=true)

會員註冊成功畫面
![AddCustomerSuccessUI](UI/AddCustomerSuccessUI.png?raw=true)

會員註冊失敗畫面
![AddCustomerErrorUI](UI/AddCustomerErrorUI.png?raw=true)

下單畫面	
![AddOrderUI](UI/AddOrderUI.png?raw=true)

訂單確認	
![ConfirmUI](UI/ConfirmUI.png?raw=true)

完成畫面	
![FinishedUI](UI/FinishedUI.png?raw=true)

後台管理商品畫面
![ProductManagerUI](UI/ProductManagerUI.png?raw=true)

🧑‍💻 Author | 作者介紹

Nicole Chen
🎓 Java 應用開發與資料庫設計愛好者
💼 應徵職務：Java 全端工程師 / 應用系統開發工程師
📧 Email: [nicole888416@example.com]
🔗 LinkedIn: [your-linkedin-url]
🌐 GitHub: [JewelryOrderProject](https://github.com/nicole888416/jewelryOrder.git)]

🎯 Resume Summary | 履歷摘要

Jewelry Store Ordering System (Java Swing + MySQL)
模擬珠寶店訂購流程的桌面應用程式，整合會員折扣、首購優惠、訂單列印與庫存管理。
展現完整的 Java 物件導向設計、MVC 架構開發與資料庫串接能力。

