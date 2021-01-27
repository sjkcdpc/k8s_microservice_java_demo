>## 这是一个基于SpringCloud的微服务架构项目

>## 部署须知
  * 1. 导入db目录下数据库文件到自己的MySQL服务器
  * 2. 修改配置环境（xxx-service/src/main/resources/application.yml，active值决定启用环境配置文件）
  * 3. 修改连接数据库配置（xxx-service/src/main/resources/application-fat.yml）
  * 4. 修改前端页面连接网关地址（portal-service/src/main/resources/static/js/productList.js和orderList.js）
  * 5. 服务启动顺序：注册中心 -> gateway -> portal -> product,stock,order

> ### 对应课程：https://ke.qq.com/course/429122
![avatar](https://github.com/lizhenliang/Shell-Python-Document/blob/master/%E8%81%94%E7%B3%BB%E6%96%B9%E5%BC%8F.jpg)
