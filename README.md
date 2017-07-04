﻿#SpringBoot集成MyBatisPlus
SpringBoot集成MyBatisPlus
集成Shiro  可以快速开发

数据库文件: /sql/wstro.sql  直接运行mysql
项目使用技术:SpringBoot Spring SpringMVC MyBatis MyBatisPlus Freemaker ApacheShiro 数据库:MySql
部署:
	application.properties更改指定部署模式还是开发模式 dev / prod  分别对应application-dev.properties  /  application-prod.properties
	修改dev / prod 文件 
		SEO:
			seo.author 作者
			seo.keywords 关键词
			seo.description 网页描述  (如果是中文，请进行Unicode转码  http://tool.chinaz.com/tools/unicode.aspx)
		
		server.port 服务端口  (部署在Tomcat上以Tomcat为准)
		server.contextPath 服务器上文文路径 请和servlet.contextPath统一   (部署在Tomcat上以Tomcat为准)
		
		spring.mail 设置邮件的端口 账号及密码
		
		spring.redis 设置Redis 服务器地址 密码 及端口
		
		spring.datasource.url 设置数据库连接信息  账号(username) 及 密码(password)


开发者:
	
	调试直接运行  com.wstro.App.java Run As  java Application
	
	打包:
		mvn运行  mvn clean package spring-boot:repackage
		最后在target目录下面生成一个war包 直接部署Tomcat运行
	
	
	此处Redis缓存注解和EhCache缓存注解只能使用1个
	使用
		@Primary标注