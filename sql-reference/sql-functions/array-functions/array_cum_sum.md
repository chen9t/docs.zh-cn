# array_cum_sum

## 功能

对数组中元素进行向前累加。

## 语法

```Haskell
array_cum_sum(array(bigint))
array_cum_sum(array(double))
```

## 参数说明

`array`：需要处理的数组。支持的type数据类型为 BIGINT(8 字节有符号整型),DOUBLE (8 字节浮点数)。

## 示例

```plain text
mysql> select array_cum_sum([11, 11, 12]);
+---------------------------+
| array_cum_sum([11,11,12]) |
+---------------------------+
| [11,22,34]                |
+---------------------------+

mysql> select array_cum_sum([cast(11.33 as double),cast(11.11 as double),cast(12.324 as double)]);
+---------------------------------------------------------------------------------------+
| array_cum_sum([CAST(11.33 AS DOUBLE), CAST(11.11 AS DOUBLE), CAST(12.324 AS DOUBLE)]) |
+---------------------------------------------------------------------------------------+
| [11.33,22.439999999999998,34.763999999999996]                                         |
+---------------------------------------------------------------------------------------+

mysql> select array_cum_sum([null,1,2]);
+---------------------------------+
| array_cum_sum([null,1,2])       |
+---------------------------------+
| [null,1,3]                      |
+---------------------------------+

mysql> select array_cum_sum(null);
+---------------------------------+
| array_cum_sum(NULL)             |
+---------------------------------+
| NULL                            |
+---------------------------------+
```

## keyword

ARRAY_CUM_SUM,ARRAY