# 版本管理的领域模型

## 模型API

`/{model_class}s/{lookup_field}/`，如`/courses/python-data-analytics/`

- `GET`: 获取最新版本的单个或者列表。
- `POST`: 创建模型及版本。
- `PUT`: 创建新版本。
- `PATCH`: 创建新版本，未填写字段拉取上一个版本并拼接。
- `DELETE`: "删除"模型，实际上是标记`is_active=False`。

## 模型版本API

`/<model_class>s/{lookup_field}/<version_related_name>/{version}`，如`/courses/python-data-analytics/versions/0.1.0/`

- `GET`: 获取全部版本，或者根据版本号字段某个版本。
- `POST`: 创建版本。
- `DELETE`: "删除"版本，实际上是标记`is_active=False`。
- `PUT`和`PATCH`暂不支持。
