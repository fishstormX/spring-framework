# Springframework
用这个项目来拆解Spring 源码

会保留原有注释并适当添加注释
fork后本仓库源代码不再更新 可能存在滞后

## 启动-web容器启动
启动阶段，通过web.xml配置监听器的class[ContextLoaderListener](spring-web/src/main/java/org/springframework/web/context/ContextLoaderListener.java),在web容器启动时会调用ContextLoaderListener的contextInitialized()方法;  
直接跳转到[ContextLoader](spring-web/src/main/java/org/springframework/web/context/ContextLoader.java)实现,调用ContextLoader的nitWebApplicationContext(ServletContext servletContext)方法,此方法返回web的IoC容器[WebApplicationContext](spring-web/src/main/java/org/springframework/web/context/WebApplicationContext.java)对象;
