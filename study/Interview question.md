# 运维工程师面试题目
### Linux
---
1. grep sed awk cut组合使用☆
```shell
grep "Error" Logfile.txt | cut -d" " -f3 |awk -F"" '{print $3}' | sed "s#name#HostName#g"
```
2. http错误码和原因
```shell
1xx：信息性状态码
2xx：成功状态码
3xx：重定向状态码
4xx：客户端错误状态码，uri不存在，权限错误等
5xx：服务器错误状态码，服务器发生错误无法处理，服务器过载
```
3. 长连接、短连接、WebSocket区别和使用场景
```shell
长连接：建立连接后，客户端和服务器保持长时间的连接。多个请求和相应可以通过同一个连接来完成，比短连接更加的高效
	keep-alive：
	数据库连接
	网络游戏
短连接：每次请求都建立一个连接，请求结束后立即关闭连接。每次请求都需要重新创建和关闭连接，实时性差。
	api请求
	不需要频繁交互的系统
	单独的web页面
websocket：建立一个持久的双向连接，双方可以随时像对方发送数据。双发可以主动发起请求而不是每次客户端发起，客户端和服务器端可以随时互相发送数据，延迟较低，效率高。
	实时通讯软件
	在线游戏
	实时数据推送
	物联网
	协作工具
```
4. nginx性能优化有哪些方式☆
```shell
1. 设置工作进程的数量worker_processes为cpu核心数量，或者设置为auto
2. 修改系统最大的文件描述符限制为65535，设置每个进程的最大连接数woker_connections为系统文件描述符数量
3. 设置事件驱动模型为epoll，能高效的处理大量的连接
4. 开启Gzip压缩
5. 开启文件缓存，
6. 设置长连接，请求头，请求体超时
7. 优化ssl，开启http2支持，优化ssl加密算法和参数
```
5. lvs、nginx、haproxy区别和使用场景☆
```shell
```
6. 僵尸进程是什么
```shell
```
7. 进程、线程、协程区别☆
```shell
```
8. 什么是nginx的异步非阻塞
```shell
```
9. linux网络丢包怎么排查☆
```shell
```
10. 常用的性能分析诊断命令☆
```shell
```
11. 什么是进程中断
```shell
```
12. 什么是软中断、硬中断
```shell
```
13. 什么是不可中断进程
```shell
```
14. 什么是栈内存和堆内存
```shell
```
15. top 命令里面可以看到进程哪些状态☆
```shell
```
16. Linux 系统中/proc是做什么的
```shell
```
17. load和cpu使用率区别
```shell
```
18. MAC地址IP地址如何转换
```shell
```
19. 常见的raid有哪些，使用场景是什么
```shell
```
20. lvm怎么划分
```shell
```
21. jvm内存如何查看
```shell
```
22. 如何管理和优化内核参数
```shell
```
23. 什么是进程最大数、最大线程数、进程打开的文件数，怎么调整☆
```shell
```
24. du和df统计不一致原因☆
```shell
```
25. buffers与cached的区别☆
```shell
```
26. lsof命令使用场景
```shell
```
27. Linux中的进程间通信的方式及其使用场景
```shell
```
28. Linux中的进程优先级与设置方法
```shell
```
29. 什么是内存分页和分段
```shell
```
30. 如何创建和管理自定义systemd服务
```shell
```
31. Linux内核模块的加载与卸载过程
```shell
```
32. ansible roles使用场景，现在有多台机器需要批量加入k8s集群，怎么实现☆
```shell
```


### Kubernetes
---
1. 谈谈你对k8s的理解☆
```shell
```
2. k8s集群架构是什么☆
```shell
```
3. 简述Pod创建过程☆
```shell
```
4. 简述删除一个Pod流程
```shell
```
5. 不同node上的Pod之间的通信过程☆
```shell
```
6. pod创建Pending状态的原因☆
```shell
```
7. deployment和statefulset区别☆
```shell
```
8. kube-proxy有什么作用☆
```shell
```
9. kube-proxy怎么修改ipvs规则
```shell
```
10. ipvs为什么比iptables效率高
```shell
```
11. pod之间访问不通怎么排查☆
```shell
```
12. k8s中Network Policy的实现原理
```shell
```
13. 探针有哪些？探测方法有哪些？
```shell
```
14. pod健康检查失败可能的原因和排查思路
```shell
```
15. k8s的Service是什么☆
```shell
```
16. metrics-server采集指标数据链路
```shell
```
17. k8s服务发现有哪些方式？
```shell
```
18. pod几种常用状态
```shell
```
19. Pod 生命周期的钩子函数
```shell
```
20. Calico和flannel区别☆
```shell
```
21. calico网络原理、组网方式
```shell
```
22. Network Policy使用场景
```shell
```
23. kubectl exec 实现的原理
```shell
```
24. cgroup中限制CPU的方式有哪些
```shell
```
25. kubeconfig存放内容
```shell
```
26. pod DNS解析流程☆
```shell
```
27. traefik对比nginx ingress优点
```shell
```
28. Harbor有哪些组件
```shell
```
29. Harbor高可用怎么实现
```shell
```
30. ETCD调优
```shell
```
31. 假设k8s集群规模上千，需要注意的问题有哪些？
```shell
```
32. 节点NotReady可能的原因？会导致哪些问题？☆
```shell
```
33. service和endpoints是如何关联的？
```shell
```
34. ReplicaSet、Deployment功能是怎么实现的？
```shell
```
35. scheduler调度流程
```shell
```
36. HPA怎么实现的☆
```shell
```
37. request limit底层是怎么限制的☆
```shell
```
38. helm工作原理是什么？
```shell
```
39. helm chart rollback实现过程是什么？
```shell
```
40. velero备份与恢复流程是什么
```shell
```
41. docker网络模式
```shell
```
42. docker和container区别☆
```shell
```
43. 如何减⼩dockerfile⽣成镜像体积？
```shell
```
44. k8s日志采集方案
```shell
```
45. Pause容器的用途☆
```shell
```
46. k8s证书过期怎么更新
```shell
```
47. K8S QoS等级☆
```shell
```
48. k8s节点维护注意事项
```shell
```
49. Headless Service和ClusterIP区别☆
```shell
```
50. Linux容器技术的基础原理
```shell
```
51. Kubernetes Pod的常见调度方式
```shell
```
52. kubernetes Ingress原理☆
```shell
```
53. Kubernetes各模块如何与API Server通信
```shell
```
54. kubelet监控worker节点如何实现
```shell
```
55. 容器时区不一致如何解决？


### Prometheus
---
1. Prometheus的工作流程
```shell
```
2. Metric的几种类型？分别是什么？☆
```shell
```
3. Prometheus有哪几种服务发现☆
```shell
```
4. Prometheus常用函数
```shell
```
5. thanos架构☆
```shell
```
6. thanos与VictoriaMetrics对比
```shell
```
7. thanos sidecar和receive区别☆
```shell
```
8. thanos rule组件和prometheus区别
```shell
```
9. Prometheus告警从触发到收到通知延迟在哪
```shell
```
10. 告警抑制怎么做☆
```shell
```
11. 告警架构高可用怎么做☆
```shell
```
12. Pod指标WSS和RSS区别☆
```shell
```
13. 监控四个黄金指标
```shell
```
14. 在大规模环境下，如何优化Prometheus性能
```shell
```
15. 如何实现告警的自动化响应☆
```shell
```
16. Prometheus数据压缩和持久化实现原理
```shell
```
17. kubectl top输出与Linux free命令不一致原因☆
```shell
```
18. 用到了哪些exporter，功能是什么
```shell
```
19. 是否自己开发过exporter☆
```shell
```
20. target down的情况如何进行故障排除？
```shell
```
22. Exporter 停止工作，如何监控？
```shell
```
23. Prometheus的拉取模式与zabbix推送模式有何区别？各有什么优缺点？
```shell
```
24. Prometheus operator怎么添加targets和告警规则
```shell
```
25. k8s集群外exporter怎么使用Prometheus监控
```shell
```


### ELK
---
1. ES写入索引原理
```shell
```
2. ES存储原理☆
```shell
```
3. 搜索文档（单个文档）流程
```shell
```
4. ES全文搜索流程
```shell
```
5. ES写入性能优化☆
```shell
```
6. ES查询性能优化☆
```shell
```
7. ES JVM使用过高如何排查
```shell
```
8. ES的Fleet server架构☆
```shell
```
9. Fleet server架构和elk架构使用场景☆
```shell
```
10. ClickHouse、loki、ES的优劣对比
```shell
```
11. ES架构☆
```shell
```
12. 业务类ES和日志类ES架构设计区别
```shell
```
13. ES Full Gc怎么排查处理
```shell
```
14. 全文检索和精确搜索区别☆
```shell
```
15. 集群变黄状态时，你会如何进行故障排除☆
```shell
```
16. 如何在集群中添加或移除节点
```shell
```
17. ES Young GC和old GC有什么区别
```shell
```
18. 怎么提高查询结果评分
```shell
```
19. ES的version是解决什么问题的
```shell
```
20. 查询数据慢如何排查优化☆
```shell
```
21. 是否对ES JVM做过调优
```shell
```
22. ES是否数据越多需要内存越大
```shell
```
23. ES集群数据备份如何实现☆
```shell
```
24. ES聚合有哪些方式
```shell
```
25. Filebeat如何保证连续发送日志
```shell
```
26. Logstash如何提升性能☆
```shell
```
27. 如何提高Filebeat性能
```shell
```
28. Filebeat如何收集容器日志
```shell
```


### Python VUE
---
1. Python中的 GIL是什么？它如何影响多线程？☆
```shell
```
2. python装饰器☆
```shell
```
3. is 和 == 的区别☆
```shell
```
4. Python中的生成器和迭代器有什么区别
```shell
```
5. Python的垃圾回收机制是如何工作的
```shell
```
6. Python上下文管理器的概念及其用途。
```shell
```
7. dict的内部实现原理
```shell
```
8. python浅拷贝和深拷贝☆
```shell
```
9. lambda匿名函数使用场景举例
```shell
```
10. 常见设计模式
```shell
```
11. python单例模式
```shell
```
12. 面向对象中__new__和__init__区别☆
```shell
```
13. Python中的列表和字典是如何实现的？它们在时间复杂度上有何差异？
```shell
```
14. Python中的多线程模块的区别☆
```shell
```
15. asyncio编写异步代码
```shell
```
16. django请求的生命周期☆
```shell
```
17. JWT认证
```shell
```
18. 什么是wsgi，uwsgi
```shell
```
19. Django安全防护
```shell
```
20. drf继承过哪些视图类，他们之间的区别☆
```shell
```
21. 谈谈django flask fastapi各自的优劣和适用场景。
```shell
```
22. python定时任务解决方案☆
```shell
```
23. 在 Celery 中，如何确保任务的可靠性和持久性
```shell
```
24. 如何监控 Celery 任务的执行情况
```shell
```
25. 当 Celery 任务出现阻塞或延迟时，你如何进行故障排除？
```shell
```
26. VUE双向数据绑定
```shell
```
27. VUE实例的生命周期钩子函数有哪些☆
```shell
```
28. v-if与v-show区别☆
```shell
```
29. cookie和seesion区别☆
```shell
```
30. VUE父子组件如何通信
```shell
```
31. nextTick 使用场景
```shell
```
32. ref和reactive区别
```shell
```
33. 你有写过VUE自定义指令吗？
```shell
```
34. 排序算法☆
```shell
```
35. 查找算法☆
```shell
```
36. SSO单点登录实现原理☆
```shell
```
### 开放性问题
---
1. 谈谈你对SRE理念的理解☆
```shell
```
2. 什么是可观测性
```shell
```
3. 你们当前的业务规模☆
```shell
```
4. 运维过程中遇到的最大的故障是什么？怎么解决的？☆
```shell
```
5. 有没有人为误操作导致故障，如何处理的？☆
```shell
```
6. 平时怎么去学习新的技术☆
```shell
```
7. 最近工作中做过最有意义的事☆
```shell
```
8. 最近研究的技术方向是什么
```shell
```
9. 运维上线流程规范
```shell
```
10. 运维体系建设包含哪些方面☆
```shell
```
11. 故障事件管控怎么设计
```shell
```
12. 告警覆盖率和准确率怎么衡量☆
```shell
```
13. 如何建设运维保障体系
```shell
```
14. 运维给公司带来的价值是什么
```shell
```
15. 运维和其他团队的职能边界和合作模式是什么
```shell
```
16. 运维的发展方向是什么☆
```shell
```
17. 运维的工作重点是什么
```shell
```
18. 运维的工作效率如何提升
```shell
```
19. 是否做过故障总结，包含哪些内容
```shell
```
20. 如何看待自动化操作高效性和人工操作确认安全性的问题
```shell
```
21. 如何看待运维维稳和开发求新的问题☆
```shell
```
22. 如何看待追求更多的可靠性和成本的平衡问题
```shell
```
23. 如何看待追求稳定性和新技术方案实践的问题
```shell
```
24. 如何看待运维工作中的重复性、没有持续价值的工作☆
```shell
```
25. 如何避免告警通知频繁导致成为告警噪声☆
```shell
```
26. 是否关注过资源使用率，考虑降低成本☆
```shell
```
27. CMDB数据库怎么设计
```shell
```
28. SLO是多少，运维自动化率多少
```shell
```
29. 与上级意见不一致怎么办
```shell
```
30. 你的优点和缺点分别是什么？
```shell
```
31. 与其他候选人相比，你的核心竞争力是什么？
```shell
```
32. 部分用户访问服务首页白屏超时，分析服务请求过程和可能的原因
```shell
```
33. 线上一个服务响应很慢，你如何排查，排查流程是什么?
```shell
```
34. 你们的告警监控体系怎么设计的？
```shell
```