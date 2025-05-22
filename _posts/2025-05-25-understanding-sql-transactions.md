---
layout: post
title: "Understanding SQL Transactions"
date: 2025-05-25
excerpt: "Learn how SQL transactions work to maintain data integrity with COMMIT and ROLLBACK."
---

SQL transactions are used to **ensure data consistency** and **handle errors** gracefully. A transaction is a set of operations that are executed as a single unit of work.

If any part of the transaction fails, the entire operation is rolled back.

## 🔹 Basic SQL Transaction Example 

```sql
BEGIN TRANSACTION;

UPDATE Accounts
SET Balance = Balance - 500
WHERE AccountID = 101;

UPDATE Accounts
SET Balance = Balance + 500
WHERE AccountID = 202;

COMMIT;
```
