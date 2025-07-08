# DYA - 2

## 大的国家 - SQL

``` C++
# Write your MySQL query statement below
select name,population,area from World where area >= 3000000 or population >= 25000000

作者：无关风月
链接：https://leetcode.cn/problems/big-countries/solutions/3718025/595-da-de-guo-jia-sql-by-wu-guan-feng-yu-7z65/
来源：力扣（LeetCode）
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。
```

## 文章浏览I - SQL

```SQL
# Write your MySQL query statement below
# 可能会有重复的错误，比如最后两个，所以需要去重
-- select author_id as id from Views where author_id = viewer_id
-- 在 SQL 中，SELECT DISTINCT 是一个组合关键字，用于返回唯一不同的值。DISTINCT 必须紧跟在 SELECT 关键字之后
select distinct author_id as id from Views where author_id = viewer_id order by id

作者：无关风月
链接：https://leetcode.cn/problems/article-views-i/solutions/3718043/wen-zhang-liu-lan-i-by-wu-guan-feng-yue-00w2b/
来源：力扣（LeetCode）
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。
```

