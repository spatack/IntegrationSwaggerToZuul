# IntegrationSwaggerToZuul
将swagger整合到网关zuul

1.添加依赖  
网关和其他微服务都要  
[spring-boot-starter-swagger](https://mvnrepository.com/artifact/com.spring4all/spring-boot-starter-swagger/1.5.1.RELEASE)  
2.配置扫包  
在需要生成swagger文档的微服务的配置文件添加扫包  
swagger:  
  base-package: com.example.controller   
3.在启动类添加注解  
@EnableSwagger2Doc   
4.在网关添加一个配置类  
见swagger文件夹下的DocumentConfig   

这个配置缺点：虽然能从网关直接访问到其他微服务的接口文档，但还不能动态获取。   
还有就是 版本较老 ，2017年后就没更新了。
