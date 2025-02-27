## CH6 - 设计一个键值数据库，1013

## 需求
- put(key, value)
- get(key)
- 类似Amazon Dynamo，Memcached，Redis
- 键值对小于10K
- 支持大数据
- 高可用性，容忍节点故障
- 高扩展性，支持大规模数据集
- 自动扩容
- 可调整的一致性
- 低延迟

## 单机键值数据库
- 使用哈希表，保存在内存
- 或者磁盘，内容里只放热点数据

## 分布式键值数据库
- CAP 理论，一致性，可用性，分区容错性
- CA 系统不存在
- 数据分区
- 数据复制
- 一致性
- 解决冲突
- 容错
- 系统架构图
- 读写路径

## 数据分区
- 一致性哈希，虚拟节点
- 数据平均分布到每个节点
- 每次节点数量改变时，数据移动量最小
- 自动扩容，根据负载自动增减节点
- 异构，每个节点都应该一样，与整个系统的负载成正比
