## 原子性 Atomicity
一個 Transaction 在寫入或更新資料時，只有全部完成或全部部完成，不會在中間結束。如有中間出錯，就會 Rollback 到 Transaction 開始前。

交易有三種基本型態

Flat Transaction、Nested Transaction與Chanied Transaction

* Flat Transaction
交易中無其他交易，為一個單元操作。
```sql
begin transaction 
    ...
end transaction
```
* Nested Transaction
 
* Chanied Transaction
交易有多個提交點，多個中斷點，若要恢復，可將動作回到上一個中斷點，而非整個較易被回復。

---
## 一致性 Consistency
交易所用的資料集合
## 隔離性 Isolation
## 持久性 Durability