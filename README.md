# java聚闪支付项目
## 安装nacos
### 下载
1.git clone https://github.com/alibaba/nacos.git 
2.mvn -Prelease-nacos clean install -U 
3.ls -al distribution/target/ 
4.cd distribution/target/nacos-server-$version/nacos/bin //change the $version to your actual path 
### 启动服务器 
#### Linux/Unix/Mac启动方式 
sh startup.sh -m standalone 
#### Ubutu或者运行脚本报错提示符号找不到，可以尝试 
bash startup.sh -m standalone 
## 外部mysql数据库支持
1.初始化mysql数据库，新建数据库nacos_config,数据库初始化文件：${nacoshome}/conf/nacos-mysql.sql 
2.修改${nacoshome}/conf/application.properties文件，增加支持mysql数据源配置，增加msyql数据源的url、用户名和密码 
spring.datasource.platform=mysql 
db.num=1 
db.url.0=jdbc:mysql://127.0.0.1:3306/nacos_config?characterEncoding=utf8&connectTimeout=1000&socketTimeout=3000&autoReconnect=true 
db.user=root 
db.password=xieqiqi037005 

