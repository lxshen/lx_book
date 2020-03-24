
# 激活指定profile

##1、在配置文件中指定

    spring.profiles.active=dev

- **使用application.properties文件启用**

```xml
1、创建dev或prod配置文件，
2、application.properaties添加
spring.profiles.active=dev/prod
```

 - **使用application.yml文件启用**

```xml
spring:
  profiles:
    active: dev
---
server:
  port: 10000
spring:
  profiles: dev
---
server:
  port: 10001
spring:
  profiles: prod
```

##2、命令行
可以直接在测试的时候，配置传入命令行参数

    java -jar spring-boot-02-config-0.0.1-SNAPSHOT.jar --spring.profiles.active=dev

##3、虚拟机参数

    -Dspring.profiles.active=dev


 