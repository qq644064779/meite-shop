# 每特教育微服务电商项目
# 版权说明:
该项目“基于SpringCloud2.x构建微服务电商项目”由每特教育|蚂蚁课堂版权所有，未经过允许的情况下，私自分享视频和源码属于违法行为。<br> 
该项目作者:97后互联网架构师-余胜军 <br> 
视频网址:http://www.mayikt.com/front/couinfo/179/0 <br> 
联系方式:微信yushengjun644、QQ644064779<br>
# 项目说明
该想项目是采用目前比较流行的SpringBoot/SpringCloud构建微服务电商项目，实现一套串联的微服务电商项目，能完全掌握该知识，可以在一线城市拿到月薪25+k薪资。<br> 
完全符合一线城市微服务电商的需求，对中国程序猿学习微服务电商架构，有非常大的帮助，该项目涵盖从微服务电商需求讨论、数据库设计、技术选型、互联网安全架构、整合SpringCloud各自组件、分布式基础设施、使Docker+k8s+jenkins实现微服务自动化部署、项目上线域名配置、SEO优化、大数据统计分析等。<br> 
注意：该项目会在2019年4月份左右上线GitHub和码云等开源网站平台。
# 技术选型

## A. 项目采用SpringBoot2.x+SpringCloud2.x构建微服务电商项目
1.使用SpringCloudEureka作为注册中心，实现服务治理<br> 
2.使用Zuul网关框架统一管理微服务请求入口<br> 
3.使用Ribbon实现本地负载均衡器和FeginHttp客户端调用工具<br> 
4.使用Hystrix服务保护框架(服务降级、隔离、熔断、限流)<br> 
5.使用消息总线Stream RabbitMQ和Kafka<br> 
6.微服务API接口安全控制与单点登陆系统CAS+JWT+Oauth2.0<br> 
## B. 分布式基础设施环境构建
1.分布式任务调度平台XXL-Job<br> 
2.分布式日志采集系统ELK +kafka<br> 
3.分布式事务解决方案LCN <br> 
4.分布式锁解决方案Zookeeper、Redis<br> 
5.分布式配置中心携程阿波罗 <br> 
6.高并发分布式全局ID生成雪花算法<br> 
7.分布式Session框架Spring-Session<br> 
8.分布式服务追踪与调用链ZipKin  <br> 

## C.项目运营与部署环境
1.分布式设施环境，统一采用docker安装<br> 
2.使用jenkins+docker+k8s实现自动部署 <br> 
3.微服务API管理ApiSwagger<br> 
4.使用GitLab代码管理 <br> 
5.统一采用第三方云数据库<br> 
6.使用七牛云服务器对静态资源实现加速<br> 
7.构建企业级Maven私服<br> 

# 系统架构


# 项目构建
## A. 分布式基础设施项目


---meite-shop-parent-----公共Pranet接口<br> 
 ----meite-shop-basics----分布式基础设施<br> 
 -----meite-shop-basics-springcloud-eureka—注册中心<br> 
 -----meite-shop-basics-apollo-config-server—阿波罗分布式配置中心<br> 
 ----meite-shop-basics-springcloud-zuul—统一请求入口<br> 
 ---meite-shop-basics-xuxueli-xxljob—分布式任务调度平台<br> 
 ---meite-shop-basics-codingapi-lcn—分布式事务解决框架<br> 
 ---meite-shop-basics-codingapi-zipKin  —分布式调用链系统<br> 
 ---meite-shop-basics-codingapi-elk  —分布式日志收集<br> 


