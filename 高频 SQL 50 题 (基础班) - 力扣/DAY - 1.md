# DAY - 1

## 可回收且低脂的产品

https://leetcode.cn/problems/recyclable-and-low-fat-products/description/?envType=study-plan-v2&envId=sql-free-50 - 可回收且低脂的产品

```SQL
# Write your MySQL query statement below
select product_id from Products where low_fats = 'Y' and recyclable = 'Y';
```

## 寻找用户推荐人

https://leetcode.cn/problems/find-customer-referee/?envType=study-plan-v2&envId=sql-free-50 - 寻找用户推荐人

首先要明确 `NULL` 值在 `SQL` 中的特殊性**: `NULL` 表示 "未知道", 不能用普通的比较运算符 (=, !=, <>) 判断, 必须用 `IS NULL` 或 `IS NOT NULL`

```SQL
select name from Customer where referee_id <> 2;
```

会漏掉 `referee_id` 为 `NULL` 的记录

`NULL<>2` 的结果是 `UNKNOWN` (既不是 `TRUE` 也不是 `FALSE`), 所以查询会自动排除 `referee_id` 为 `NULL` 的行

```SQL
select name from customer where referee_id = null or referee_id <> 2;
```

`referee_id = null`永远为`UNKNOWN`，导致这部分条件失效。

判断`NULL`必须用`IS NULL`，不能用`=`，`referee_id = null`是语法错误的写法。