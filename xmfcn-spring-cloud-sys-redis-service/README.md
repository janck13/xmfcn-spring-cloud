## 一、工程职责：

1、Redis相关的功能服务，负责Redis缓存相关功能，全局ID统一分配功能，分布式锁功能和其他Redis支持的功能。

2、支持单条消息缓存暂不支持批量消息缓存

3、此工程为其他业务功能提供Redis相关的。

## 一、拆分原因：

1、仅仅提供Redis相关的服务功能，且访问量可能比较大，特别是缓存和分布式锁相关的功能，调用端应该尽量减少RPC请求，减缓服务压力。
增加服务节点的数量可以提高服务能力，当然，这还取决于Redis本身的能力。

2、提供分布式锁实现