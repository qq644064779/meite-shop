# 每特教育微服务电商项目
# 版权说明:
该项目“基于SpringCloud2.x构建微服务电商项目”由每特教育|蚂蚁课堂版权所有，未经过允许的情况下，私自分享视频和源码属于违法行为。<br> 
该项目作者:97后互联网架构师-余胜军 <br> 
视频网址:http://www.mayikt.com/front/couinfo/189/0 <br> 
联系方式:微信yushengjun644、QQ644064779、644064065<br>
# 项目说明
该想项目是采用目前比较流行的SpringBoot/SpringCloud构建微服务电商项目，实现一套串联的微服务电商项目，能完全掌握该知识，可以在一线城市拿到月薪25+k薪资。<br> 
完全符合一线城市微服务电商的需求，对中国程序猿学习微服务电商架构，有非常大的帮助，该项目涵盖从微服务电商需求讨论、数据库设计、技术选型、互联网安全架构、整合SpringCloud各自组件、分布式基础设施、使Docker+k8s+jenkins实现微服务自动化部署、项目上线域名配置、SEO优化、大数据统计分析等。<br> 

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
3.分布式事务解决方案Rabitmq <br> 
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
--meite-shop-parent-----公共Pranet依赖<br> 
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
---meite-shop-api-dto 开放接口实体类层<br> 
-----meite-shop-service-api-weixin-dto 微信实体类<br> 
-----meite-shop-service-api-member-dto  会员实体类<br> 
-----meite-shop-service-api-sso-dto  sso实体类<br> 
-----meite-shop-service-api-item-dto  商品实体类<br> 
-----meite-shop-service-api-search-dto 搜索实体类<br> 
-----meite-shop-service-api-pay-dto 聚合支付实体类<br> 
-----meite-shop-service-api-order-dto 订单实体类<br> 
-----meite-shop-service-api-spike-dto秒杀实体类<br> 
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
第一节	需求讨论与技术架构选型 <br> 
第二节	微服务架构环境搭建Maven私服仓库 <br> 
第三节	微服务架构环境搭建GitLiab代码仓库 <br> 
第四节 搭建企业级微信公众号平台 <br> 
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



# 项目核心技术点说明:
## 每特微服务电商平台-会员服务/SSO服务

 ```
1. 负责创建会员服务和SSO单点登陆系统项目   
2. 负责会员服务核心模块开发(令牌Token登陆和多端唯一登陆接口的开发)
3. 负责会员服务QQ和微信联合登陆功能开发
4. 负责SSO单点登陆系统的开发
1.令牌登陆实现:
客户端（移动端、PC端、微信端）调用会员服务登陆接口成功后，返回对应的Token令牌，有效期为90天，客户端保存该Token信息，客户端使用令牌关联用户会话信息。
使用UUID随机生成Token令牌、用户登陆成功后会生成对应的Token令牌作为key，存入在Redis中，Redis中令牌对应的Value为UserId、有效期为90天。
2.唯一登陆实现:
 2.1后端实现：使用数据库表记录每次客户端登陆的Token令牌，每次产生新的用户Token都会删除上一次登陆的Token，客户端采用定时器检查当前客户端保存的Token是否过期或者是否重复登陆。
 2.2前端实现：采用定时器形式，使用Token调用验证接口是否已经过期。
3.联合登陆实现：
 调用腾讯/微信开放平台，使用OAuth2.0授权获取用户相关openid，使用openid关联会员服务账号信息
4.SSO登陆实现:
 使用XXL-SSO框架实现微服务平台单点登陆开发
 ```
## 每特微服务电商平台-商品搜索服务
 ```
1.	负责整个商品数据库的设计  
2.	负责商品搜索服务接口的开发
3.	负责实现Elasticsearch与MySQL数据库同步问题
4.	负责商品详情页面静态化开发

 1.商品数据库设计: 
分类表采用无限级分类策略，采用SPU(产品单元)、SKU(库存量单元)具体商品规格。
  2.商品搜索服务接口:
 为了提高用户的搜索效率，采用Elasticsearch存放商品信息数据，集成IK分词+PingYin插件，实现拼音和中文分词高效查询。
  3.MySQL与ES数据同步:
    3.1采用MQ实时性和Logstash定时实现MySQL与ES同步
    3.2MQ同步方案:发布/修改/删除/商品的时候，以MQ异步形式同步到Elasticsearch中，可以实时保证双方数据一致性问题。
    3.3Logstash同步方案:使用Logstash定时方式读取数据库最新的数据>=update_time时间 ，让后在格式化成json格式输出到
Elasticsearch中。
  4.商品详情页面静态化:
  5.使用Nginx+ FreeMarker实现页面的静态化、Nginx+Lua+OpenResty
   ```
## 每特微服务电商平台-聚合支付平台
   ```
1.	与第三方支付接口平台技术人员对接
2.	聚合支付平台数据库表结构设计
3.	基于设计模式构建聚合支付平台
4.	基于MQ实现分布式事务解决方案
5.	使用xxl-job实现聚合支付对账
6.	常用遇到支付难题问题解决 

1.与第三方支付接口平台技术人员对接
 负责支付宝、微信支付、银联支付等支付接口技术人员沟通对
2.聚合支付平台数据库表结构设计
 负责聚合支付平台数据库表结构设计，payment_channel渠道表、payment_transaction流水表、payment_transaction_log日志表等实现完全可视化界面支付开关控制支付渠道。
3.基于设计模式构建聚合支付平台
使用策略+工厂设计模式实现支付接口提交html表单元素重构、使用模版方法+工厂设计模式实现共同异步回调代码重构，采用多线程+MQ实现支付回调日志收集
4.使用xxl-job实现聚合支付对账
使用分布式任务调度平台XXL-JOB实现支付接口产生延迟导致订单状态不同步实现自动化补偿，每天晚上两点钟时间定时触发任务，商户端主动使用支付id调用第三方支付渠道接口查询支付状态是否已经支付过，如果第三方支付渠道接口已经支付过，同步商户端订单状态。 
 5.基于MQ实现分布式事务解决方案
在微服务系统中，支付服务调用积分服务接口增加对应积分，该场景存在分布式事务问题，我们采用rabbitMQ实现+补单形式保证最终一致性实现双方数据同步
6.常用遇到支付难题问题解决 
问题1：支付回调接口中，产生延迟通知？导致支付状态不一致问题 
 解决方案：商户端使用任务调度平台主动调用第三方接口查询，实现数据同步
问题2：重试支付回调接口时，如何保证回调接口通知幂等性问题
 解决方案：因为第三方支付接口采用间隔性重试机制，使用支付全局id查询支付状态已经支付，及时响应成功状态通知给第三方支付平台不在继续重试。
问题3：支付金额与商品金额如果不一致时，如何处理
 解决方案：在支付回调中查询待支付表记录金额与实际回调金额是否一致，如果不一致该笔订单纳为异常订单
问题4：第三方支付平台如何与对接系统保证分布式事务问题
 解决方案：使用重试+补偿+日志记录形式保证最终一致性实现数据的统一
问题5：支付服务如何与其他系统保证分布式事务问题
  解决方案：MQ/TCC/LCN分布式事务解决框架解决分布式事务问题
  ```
  
 ## 每特微服务电商平台-微服务秒杀抢购商品
### 责任描述
1.	秒杀抢购实现方案技术选型<br>
2.	负责前端静态资源带宽优化<br>
3.	负责核心秒杀接口代码编写<br>
### 技术描述
秒杀抢购实现方案技术选型<br>
前端：<br>
 七牛云静态资源服务器+CDN内容分发实现减少服务器带宽资源、复杂验证码<br>
后端：<br>
网关实现安全过滤、幂等、高并发、限流、用户频率设计 、基于MQ+库存令牌桶实现防止超卖和减少数据库IO的操作<br>
 负责前端静态资源优化<br>
1、	使用maven插件自动对静态资源实现压缩、每次发布的时候使用版本号码更新静态资源<br>
2、	将页面静态资源(css、js、img)等，存放到七牛云静态资源服务器，七牛云静态资源能够实现CDN内容分发，将静态资源缓存到全国各地节点，能够减少服务器的带宽传输，从而提高带宽传输速度。<br>
负责核心秒杀接口代码编写<br>
  网关:<br>
1.	基于责任链设计模式实现对网关权限控制实现动态开关<br>
2.	使用guava RateLimiter 令牌桶算法实现对秒杀接口限流<br>
3.	使用redis的setnx命令实现对用户频率限制<br>
 后台运营:<br>
1.每次发布商品的时候，提前在redis中生成好对应相等的库存令牌<br>
 秒杀接口：<br>
1.	使用histrx对秒杀接口实现服务隔离防止雪崩效应<br>
2.	从redis中获取对应商品的令牌，只要能够抢到令牌就能够秒杀成功<br>
3.	使用异步形式RabbitMQ实现对商品的库存修改<br>
4.	使用乐观锁机制(版本号)+库存>0判断防止库存超卖问题<br>





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







# 学员练习常见问题

### 1.下载微服务电商项目依赖SpringCloudJar包，Jar包明明真实存在，却启动报错找不到该类
解决办法：首先MavenUpdate，如果还不行，就开始清空Maven仓库，重新下载Jar包即可。<br> 

### 2.将本地Jar包打包到Maven私服仓库中，无法上传本地Jar包。
解决办法：maven工程的version版本必须是 RELEASE版本<br> 
具体说明：将改成0.0.1-SNAPSHOT改成 0.0.1-RELEASE重新上传即可<br> 

### 3.将本地Jar包打包到Maven私服仓库中，上传Jar包报错401
解决办法：401说明权限不足，检查配置的账号权限策略<br> 

### 4.外网服务器构建阿波罗分布式配置中心，注册中心的地址是内网IP，导致无法和客户端通讯
解决办法:在Demo.sh文件中，修改注册IP为内网IP即可。<br> 

