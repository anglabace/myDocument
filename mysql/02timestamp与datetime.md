# timestamp与datetime

## 1. 两者存储方式不一样

timestamp 把客户端插入的时间从当前时区转换为utc(世界标准时间)，查询时，再转换为客户端时区时间

datetime 不做任何改变

如果有跨时区业务，可以选择timestamp存储

## 2. 时间范围不一样

timestamp 时间范围为：'1970-01-01 00:00:01.000000' 到 '2038-01-19 03:14:07.999999'

datetime 时间范围为：'1000-01-01 00:00:00.000000' 到 '9999-12-31 23:59:59.999999'