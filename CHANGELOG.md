# 更改日志

## [3.1.0] - 2024-06-15
此版本修改主要是代码内部结构，普通用户应可以无感升级。

 - 【更改】优化上传结果查询输出格式，此修改仅影响格式化 (Pretty) 输出，使用 `--json` 获取原始 JSON 数据的输出不受影响。
 - 【更改】优化上传进度输出，上传进度显示人类可读的文件大小。
 - 【重构】重写 S3 上传类，使用 Dataclass 在程序主体、数据库类和 S3 类之间传递数据。


## [3.0.0] - 2024-06-10
从 `cos-uploader` 修改而来，原版本号为 `2.x`，因此此程序版本号从 `3.0.0` 开始。

 - 【新增】支持 AWS S3 和阿里云 OSS，理论上其他 S3 兼容服务也支持。
 - 【更改】将上传历史储存从 NDJSON 改为 SQLite。此修改不兼容旧版本。
