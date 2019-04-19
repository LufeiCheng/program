## mongo一些高级操作

* 聚合分组查询数据量

* ```js
  db.getCollection('exam_download').aggregate([
      {$match: {'has_download': false}},
      {$group: {'_id': {'period': '$period', 'subject': '$subject'}, 'count': {'$sum': 1}}}
  ])
  ```

  

