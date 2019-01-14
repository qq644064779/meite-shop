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

<div align=center><img  src="https://github.com/qq644064779/meite-shop/blob/master/%E6%AF%8F%E7%89%B9%E6%95%99%E8%82%B2.jpg"/></div>

# 项目构建
#### A. 分布式基础设施项目
--meite-shop-parent-----公共Pranet接口<br> 
 ---meite-shop-basics----分布式基础设施<br> 
 -----meite-shop-basics-springcloud-eureka—注册中心<br> 
 -----meite-shop-basics-apollo-config-server—阿波罗分布式配置中心<br> 
 -----meite-shop-basics-springcloud-zuul—统一请求入口<br> 
 -----meite-shop-basics-xuxueli-xxljob—分布式任务调度平台<br> 
 -----meite-shop-basics-codingapi-lcn—分布式事务解决框架<br> 
 -----meite-shop-basics-codingapi-zipKin  —分布式调用链系统<br> 
 -----meite-shop-basics-codingapi-elk  —分布式日志收集<br> 
#### B. 公共服务接口层
---meite-shop-service-api提供公共接口<br> 
-----meite-shop-service-api-weixin 微信服务接口<br> 
-----meite-shop-service-api-member会员服务接口<br> 
-----meite-shop-service-api-sso  sso服务接口<br> 
-----meite-shop-service-api-item商品服务接口<br> 
-----meite-shop-service-api-search 搜索服务接口<br> 
-----meite-shop-service-api-pay聚合支付平台<br> 
-----meite-shop-service-api-order订单服务接口<br> 
-----meite-shop-service-api-spike 秒杀服务接口<br> 

#### C. 公共服务接口实现层
---meite-shop-service-impl公共接口的实现<br> 
-----meite-shop-service-weixin 微信服务接口实现<br> 
-----meite-shop-service-member会员服务接口实现<br> 
-----meite-shop-service-api-sso  sso服务接口实现<br> 
-----meite-shop-service-tem商品服务接口实现<br> 
-----meite-shop-service-search 搜索服务接口实现<br> 
-----meite-shop-service-pay聚合支付平台接口实现<br> 
-----meite-shop-service-order订单服务接口实现<br> 
-----meite-shop-service-api-spike 秒杀服务接口<br> 

#### D. 公共服务接口实体类
---meite-shop-api-entitys-api 开放接口实体类层<br> 
-----meite-shop-service-api-weixin-api 微信实体类<br> 
-----meite-shop-service-api-member-api 会员实体类<br> 
-----meite-shop-service-api-sso-api  sso实体类<br> 
-----meite-shop-service-api-item-api 商品实体类<br> 
-----meite-shop-service-api-search-api 搜索实体类<br> 
-----meite-shop-service-api-pay-api 聚合支付实体类<br> 
-----meite-shop-service-api-order-api 订单实体类<br> 
-----meite-shop-service-api-spike-api  秒杀实体类<br> 
#### E. 门户平台
---meite-shop-portal 门户平台<br> 
-----meite-shop-portal-web 门户网站 <br> 
-----meite-shop-portal-sso 单点登陆系统 <br> 
-----meite-shop-portal-search 搜索系统<br> 
-----meite-shop-portal-spike 秒杀系统<br> 
-----meite-shop-portal-cms 运营系统 <br> 

#### F. 工具类

---meite-shop-common 工具类<br> 
-----meite-shop-common-core—核心工具类<br> 
-----meite-shop-common-security-安全<br> 
#### G. 分布式任务调度实现

---meite-shop-service-job 分布式定时任务调度<br> 
-----meite-shop-service-weixin-job 微信定时任务<br>
-----meite-shop-service-member-job 会员定时任务<br> 
-----meite-shop-service-tem-job 商品定时任务<br> 
-----meite-shop-service-search-job 搜索定时任务<br> 
-----meite-shop-service-order-job 订单定时任务<br> 
-----meite-shop-service-api-spike-job 秒杀定时任务<br> 

# 环境要求
为了能够更好的学习互联网微服务架构，该项目对环境要求非常高，建议电脑配置CPU在I5、32GB内存或者电脑采用集群化部署。<br> 
1.JDK统一要求:JDK1.8K <br> 
2.Maven 统一管理Jar<br> 
3.统一采用Docker安装软件<br> 
4.编码统一采用为UTF-8<br> 
5.开发工具IDE或者Eclipse<br> 

# 课程安排
第一节	需求讨论与技术架构选型 (已经完成)<br> 
第二节	微服务架构环境搭建Maven私服仓库 (已经完成)<br> 
第三节	微服务架构环境搭建GitLiab代码仓库 (已经完成)<br> 
第四节 搭建企业级微信公众号平台 (已经完成)<br> 
第五节	构建微服务电商项目与数据库实战设计<br> 
第六节	分布式基础设施之分布式配置中心环境搭建<br> 
第七节	微服务电商项目-会员服务-联合登陆<br> 
第八节	微服务电商项目-会员服务-唯一登陆<br> 
第九节	微服务电商项目-会员服务-SSO联合登陆<br> 
第十节	微服务电商项目-微服务公众号-构建微信公众号<br> 
第十一节	微服务电商项目-消息服务平台-消息服务平台<br> 
第十二节	微服务电商项目-前端技术-VUE<br> 
第十三节	微服务电商项目-商品服务-数据设计<br> 
第十四节	微服务电商项目-商品服务-搜索服务<br> 
第十五节	微服务电商项目-商品服务-购物车设计<br> 
第十六节	微服务电商项目-订单服务-订单服务<br> 
第十七节	微服务电商项目-聚合支付-数据设计<br> 
第十八节	微服务电商项目-聚合支付-银联支付<br> 
第十九节	微服务电商项目-聚合支付-支付宝支付<br> 
第二十节	微服务电商项目-秒杀服务-秒杀抢购<br> 
第二十一节	微服务电商项目-后台运营平台设计<br> 
第二十二节	微服务电商项目ELK日志分析<br> 
第二十三节	微服务电商项目安全架构<br> 
第二十四节	微服务电商项目静态资源CDN加速<br> 
第二十五节	使用jenkins+docker+k8s实现自动部署<br>
第二十六节	微服务电商项目上线部署环境<br> 
第二十七节	微服务电商项目大数据用户行为分析<br> 
最终以实际课程表格为准。<br> 

# 项目启动说明
## 分布式基础设施环境搭建
### 分布式阿波罗配环境搭建
 使用阿波罗统一管理微服务配置文件，每个服务对应阿波罗一个appid，阿波罗中的appid和微服务项目的spring.application.name保持一致<br>
#### 阿波罗环境搭建搭建
 ```
1.下载aploll配置中心 https://github.com/nobodyiam/apollo-build-scripts 
2.上传apollo-build-scripts-master文件到服务器中
3.创建阿波罗需要的数据库apolloConfigDb和apolloPortalDb
4.unzip apollo-build-scripts-master.zip 解压配置文件
5.如果没有unzip命令的话，安装zip插件 yum -y install zip unzip
6.修改demo.sh中的数据库账号和密码
7.启动阿波罗 ./demo.sh start 
 ```
 #### 修改阿波罗客户端application.properties与自己搭建的保持一致
 ```
### 阿波罗平台appid 
app.id=app-mayikt-weixin
### 阿波罗平台地址
apollo.meta=http://192.168.212.240:8080
### 开启读取多个namespaces
apollo.bootstrap.enabled = true
apollo.bootstrap.namespaces = application,mayikt.weixin
 ```
  #### 可以在C:\opt\data\appid名称查看阿波罗本地文件缓存
### 分布式事务框架LCN
### 分布式日志收集ELK



# 学员练习常见问题

## 1.下载微服务电商项目依赖SpringCloudJar包，Jar包明明真实存在，却启动报错找不到该类
解决办法：首先MavenUpdate，如果还不行，就开始清空Maven仓库，重新下载Jar包即可。<br> 

## 2.将本地Jar包打包到Maven私服仓库中，无法上传本地Jar包。
解决办法：maven工程的version版本必须是 RELEASE版本<br> 
具体说明：将改成0.0.1-SNAPSHOT改成 0.0.1-RELEASE重新上传即可<br> 

## 3.将本地Jar包打包到Maven私服仓库中，上传Jar包报错401
解决办法：401说明权限不足，检查配置的账号权限策略<br> 

## 4.外网服务器构建阿波罗分布式配置中心，注册中心的地址是内网IP，导致无法和客户端通讯
解决办法:在Demo.sh文件中，修改注册IP为内网IP即可。<br> 

