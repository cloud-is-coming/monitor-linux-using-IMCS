# monitor-linux-using-IMCS
最近，混合云的概念备受关注，在跟合作伙伴交流时，他们都很关心混合云的解决方案。这不奇怪，云虽然是大势所趋，但是由于目前大家对公有云的接受程度、相关政策的影响，以及IT基础设施的发展程度（尤其是网络带宽）等原因，用户不可能把所有系统都搬到公有云上，普遍的做法是，将一些外围应用迁到公有云上，将核心应用都保留在自己的数据中心，混合云才是主流，我相信十年之内，这种状况都不会改变。

那么问题来了，对于运维人员来说，混合云环境的运行维护将是一大挑战。去年下半年，在跟合作伙伴交流时，他们问到了这样一个问题：“我们的客户IT环境很复杂，他们不仅有自己的数据中心，另外还有一部分应用运行在IDC托管机房里，最近他们还计划在##云上租几台云主机跑某某应用，这种IT环境怎么运维啊？ 不知道是哪个倒霉蛋会接手？” 据我所知，这个合作伙伴极有可能会很成为这个“倒霉蛋”，因为客户的核心应用就是这家公司的开发的，所以客户也就顺理成章的把数据中心的运维工作交给了他们。

不知道这家公司到最后有没有成为“倒霉蛋”，不过现在老余倒是要给他们5字箴言：“那都不是事！”

因为老余发现了一个监控神器，它可以同时监控本地和云上的基础设施，而且是通过统一、全景式的可视化方式进行监控，这个神器就是Oracle最近推出的基础架构监视云服务（Infrastructure Monitoring Cloud Service，简称IMCS）。

偷个懒，先用官方的广告语来介绍这个服务。
服务名称
Infrastructure Monitoring Cloud Service（基础架构监视云服务），简称IMCS。

**监控能力**

**1.监控目标**


- 主机，包括Linux, Solaris, Windows, AIX。 
- 关系型和非关系型数据库，包括Oracle Database, MySQL, Microsoft SQL Server, MongoDB。
- 应用服务器，包括Oracle WebLogic Server, Tomcat, Apache HTTP Server。
- 容器，包括Docker Engine, Docker Container。
- 网络设备，包括Cisco Catalyst Switch, Oracle Traffic Director。
- 云服务，包括Oracle Cloud Compute, Oracle Database Cloud Service, Oracle Java Cloud Sevrice, Amazon EC2。


**2.提供相应仪表板展示IT基础设施健康度的历史视图，**
包括：
- 受控的实体总数，并允许下钻式 查看详情。 
- 实体启动、关闭的数量。
- 按严重级别统计告警数量，包括：致命告警、紧急告警、一般告警三级。也同时显示周期内告警数量的增加或减少。
- 性能与状态监控，包括主机、数据库、应用服务器、容器、网络等。



**3.使用者可以进一步调查告警的详细情况。**

**4.提供散点图展示IT基础设施负载的分布，例如对主机性能，可通过CPU和内存使用量图示化地展示哪些主机负载最大、哪些主机负载很小。散点图的指标可以由使用者自己选择。**

**5.针对受控IT基础设施提供特定的指标监控、可用性监控。**

**6.为来自于不同的供应商但属于同类的IT基础设施提供统一的监控标准。例如，对所有关系型数据库，无论是Oracle还是SQL Server还是没有SQL，可以设置统一的表空间监控指标、阈值并告警。**

**7.允许用户创建告警规则：** 
- 规则可以应用到所有实体或部分实体。
- 可以添加或修改规则条件。 
- 允许可视化告警消息或清除消息。 
- 允许定义告警通知接收人以及告警状态改变通知。

**8.提供REST API并允许创建新的监控实体、监控指标，并利用API上载监控数据等。**


**部署架构图**

![IMCS架构图](https://github.com/cloud-is-coming/monitor-linux-using-IMCS/blob/master/imcs%20architect%201.jpg)
