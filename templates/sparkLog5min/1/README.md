五分钟日志spark 计算任务
=====

## spark 版本
- spark-2.0.2-bin-hadoop2.7

- 应用使用三个镜像实例,分别为:
	- spark-master  spark master节点
	- jobs	      任务运行的镜像卷
	- spark-worker  spark worker节点


## 说明
1. 默认master节点 同时启用worker 进程
2. jobs 作为master 实例的从容器启动
3. jobs 需要指定以下环境变量
    - MASTER_IP
    - MASTER_HOST
    - HDFS_PATH
4. jobs 节点默认挂载/opt/jobs 目录
5. worker节点需要指定 SPARK_MASTER 环境变量

## 运行任务
- 脚本目录: /opt/jobs/start_josb.sh
