# 尚硅谷SpringCloud-Alibaba(三)-项目搭建

![使用idea创建maven聚合项目.png](../../../images/java/尚硅谷springcloud/3-项目搭建/使用idea创建maven聚合项目.png)

![约定大于配置.png](../../../images/java/尚硅谷springcloud/3-项目搭建/约定大于配置.png)
调完settings里面utf-8  

-----

![配置lombox.png](../../../images/java/尚硅谷springcloud/3-项目搭建/配置lombox.png)

settings->build,execution,deployment->annotation processors打勾  
Enable annotation processing (启用注释处理)  

-----

![更改jdk版本.png](../../../images/java/尚硅谷springcloud/3-项目搭建/更改jdk版本.png)
java compiler 这里改为 8  

-----

创建项目7要素  

1.建立module  
2.改POM  
3.写YML  
4.主启动  
5.业务类  
6.测试  
7.总结  

![服务示意图.png](../../../images/java/尚硅谷springcloud/3-项目搭建/服务示意图.png)
上图是常见的RESTful API风格 80端口调用微服务8001端口的逻辑层  

![img.png](../../../images/java/尚硅谷springcloud/3-项目搭建/项目结构图.png)