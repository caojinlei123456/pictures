# Hive常用函数

[toc]



## timestamp

### to_date(获取日期部分)

```
select * from dwd_face_feature where to_date(cap_time)='2020-08-01' limit 100
```

