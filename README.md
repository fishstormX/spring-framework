# <img src="src/docs/spring-framework.png" width="80" height="80"> Spring Framework [![Build Status](https://ci.spring.io/api/v1/teams/spring-framework/pipelines/spring-framework-5.3.x/jobs/build/badge)](https://ci.spring.io/teams/spring-framework/pipelines/spring-framework-5.3.x?groups=Build")
看Spring 源码

## 启动
启动阶段，通过web.xml配置监听器[ContextLoaderListener](spring-web/src/main/java/org/springframework/web/context/ContextLoaderListener.java) 
会调用ContextLoaderListener的contextInitialized()方法,
直接跳转到[ContextLoader](spring-web/src/main/java/org/springframework/web/context/ContextLoader.java)实现
调用ContextLoader的nitWebApplicationContext(ServletContext servletContext)方法
