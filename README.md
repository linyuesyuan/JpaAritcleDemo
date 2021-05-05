# JpaAritcleDemo
參考書本 Spring boot 範例實作

## 專案介紹
本專案使用MySQL作為資料庫，實作Jpa新增、查詢、修改、刪除。


## 啟動教學
- 下載本專案
- 建立本地資料庫
  - 開啟 MySQL Workbench
  - 新增 MySQL Connections
    - 輸入Connections name，並輸入帳號密碼後完成
    - 開啟剛新增的Connections
  - 新增資料庫
    - 於 Schemas 列表空白處，右鍵"Create Schemas..."
    - 於 Schemas Name 輸入 Book
    - Character Set 選擇 "utf8"，點擊Apply
- 啟動專案導入IDE開啟，或打包成jar檔(以IntelliJ IDEA為例)
  - 選擇 Open ，並選擇專案位置
  - 設定專案
    - 開啟 JpaArticleDemo/src/main/resources/application.properties 檔案
    - 修改資料庫設定
      輸入新增MySQL Connections設定的帳密
      spring.datasource.username
      spring.datasource.password
    - 若不是使用MySQL則需要修改以下欄位值
      spring.jpa.properties.hibernate.dialect
    - 修改後儲存
  - 啟動專案點擊左上角綠色箭頭符號
  - 或者打包成.jar
    - 選擇 "File | Project Structure"
    - 點選右邊列表 "Artifacts"
    - "+" -> "JAR" -> "From modules with dependecies"
    - 於Main Class 選擇本專案，並選擇"OK"
    - 於右方Maven中本專案的Lifecycle點擊"clean"
    - 再點擊"package"
    - 完成後本專案jar檔路徑位於於"Building jar:"後
    - 開啟cmd，啟動專案
      輸入指令 cd 檔案鎖在資料夾路徑
      輸入指令 java -jar 檔案名稱
    - 啟動完成
    - 於網頁中輸入http://localhost:8080/article/add 新增文章名稱及內容
    - 文章列表 http://localhost:8080/article/ 
 
  
