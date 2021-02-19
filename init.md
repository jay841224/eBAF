# eBAF 處理 SQL
## 初始
---
### 建立 SQL 檔案
---
### DAO
1. DAO 建構子必要變數 fieldName(table 的 column)
* 包含3個時間相關之 String[] 和 1 個 general 的 String[]
* 還有一個為 fieldName_all (包含上述全部的 fieldName)
---
### 新增變數儲存 SQL 的連線位址
---
### Override insert、update、delete 等方法
### 在方法中取得連線
1. 主要方法
```java
DataSet ds = Transaction.getDataSet();
```
2. 一般不使用的方法
```java
DataSet ds = Transaction.getDynamicDataSet();
```
---
### 處理資料
1. 新增、修改
```java
executeUpdate("需求的Map", SQL_INSERT_001, true, true, ds);
```
2. 查找
```java
//reutrn List<Map>
VOTool.findToMaps(ds, SQL);

//return Map
VOTool.findOneToMap(ds, SQL);
```
