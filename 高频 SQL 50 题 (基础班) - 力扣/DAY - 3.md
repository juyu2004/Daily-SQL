# DAY - 3

## 无效的推文

```SQL
# Write your MySQL query statement below
select tweet_id from Tweets where char_length(content) > 15;

作者：无关风月
链接：https://leetcode.cn/problems/invalid-tweets/solutions/3719591/1683-wu-xiao-de-tui-wen-by-wu-guan-feng-dnzoh/
来源：力扣（LeetCode）
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。
```

char_length 函数：此函数用于统计字符串里字符的数量。无论字符占用多少字节，每个字符都算作 1。比如，对于包含中文、日文等多字节字符的字符串，char_length 会依据实际的字符个数来返回结果。

length 函数：该函数是对字符串的字节长度进行计算。由于不同的字符编码所占用的字节数不一样，所以其返回值会因编码的不同而有所差异。例如：

在 latin1 编码中，每个字符占 1 字节，此时 length 和 char_length 的结果可能相同。

而在 utf8mb4 编码中，一个汉字通常占用 3 到 4 字节，那么 length 的返回值就会大于 char_length。

## 使用唯一标识码替换员工ID

````SQL
# Write your MySQL query statement below
select e2.unique_id,e1.name 
from Employees e1
left join EmployeeUNI e2 
on e1.id = e2.id;

作者：无关风月
链接：https://leetcode.cn/problems/replace-employee-id-with-the-unique-identifier/solutions/3719207/shi-yong-wei-yi-biao-shi-ma-ti-huan-yuan-9kgr/
来源：力扣（LeetCode）
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。
````

在 SQL 查询里，`LEFT JOIN`（左连接）是一种常用的连接方式，其主要作用是返回左表（在这个例子中是 `Employees` 表）中的所有记录，不管这些记录在右表（`EmployeeUNI` 表）中是否存在匹配项。而对于那些在右表中没有匹配的记录，查询结果里右表的字段会显示为 `NULL`。