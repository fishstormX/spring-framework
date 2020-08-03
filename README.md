#Springframework
用这个项目来拆解Spring 源码

## 启动
启动阶段，通过web.xml配置监听器的class[ContextLoaderListener](spring-web/src/main/java/org/springframework/web/context/ContextLoaderListener.java),在web容器启动时会调用ContextLoaderListener的contextInitialized()方法   
直接跳转到[ContextLoader](spring-web/src/main/java/org/springframework/web/context/ContextLoader.java)实现   
调用ContextLoader的nitWebApplicationContext(ServletContext servletContext)方法    
