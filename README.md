# bookstore电商书城系统说明
- ## 目的与缺陷
  - 目的: 在校学习，进一步熟悉Spring Boot开发模式，熟悉开发流程。
  - 缺陷: 购物车和订单不能分店铺统计和付款；界面较为简陋；另外还有许多地方的用户体验性也不好；富文本编辑器那边没有实现文件上传的功能；并没有完全符合       restful api风格等等。
- ## 依赖环境
  - jdk1.8,maven,mysql
  - 注意事项
    - 在数据库中创建名为`bookstore`数据库,然后运行项目的`resource`目录下的sql脚本，记得在`application.properties`改数据库配置信息
    - 登录系统的账号和密码，请自行查看数据库下的`user`表
    - `application.properties`中的邮箱配置要改成自己，否则不能注册系统账号
- ## 系统划分与功能
  - 该系统分为前台展示和后台管理两大模块。  
  - 前台主要是为消费者服务。该子系统实现了注册，登录，以及从浏览、下单到支付的整个流程，支付使用的是支付宝的沙箱环境，属于模拟环境。需要注册沙箱账号才能      付款。  
  - 后台主要是为商家服务，实现了权限管理，店铺、商品和订单等的管理，以及生成一些简单的报表信息。访问`/admin`进入后台  
- ## 使用框架
  - 后台主要是springboot+mybatis+shiro...，前端界面主要使用bootstrap框架搭建，并使用了ueditor富文本编辑器、highcharts图表库  
- ## 运行项目
  - 方法一：在ide(推荐idea)运行项目,配置好启动环境，直接运行main方法
  - 方法二: 用springboot插件运行项目   
    在项目根目录下,运行以下maven命令  ```mvn spring-boot:run```
  - 方法三: 在ide或直接用maven打成的war包放到tomcat运行,具体操作可以百度，google
  - 方法四: 使用命令运行jar或war  
    ```java -jar xxx.jar```
  - 具体可以自行搜索`Spring Boot`项目的启动方式
