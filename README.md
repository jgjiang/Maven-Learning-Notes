# Maven-Learning-Notes
=============================
## 1. maven介绍及环境搭建
### maven概念 ###
* Maven是基于项目对象模型（POM），可以通过一小段描述信息来管理仙姑的构建、报告和文旦的软件项目管理工具.
  * bin目录是包含mvn的运行脚本
  * boot目录包含一个类加载器的框架，maven使用它加载自己的类库
  * conf配置文件
  * 在lib包含maven运行时的依赖类库
  
* mac ox 命令行安装：`brew install maven`

### maven项目目录简版 ###
```
项目名
		-src 
		   -main
		        -java
		             -package
		   -test
		        -java
		             -package
		-pom.xml
```


### maven常用命令 ###
* `mvn -v` 查看maven版本
* `mvn compile` 编译 （编译源代码，如果需要包，去pom.xml里找依赖，如果本地仓库有，就加载到classpath里。如果本地没有，就去maven网上仓库下载）
* `mvn test` 测试
* `mvn package` 打jar包
* `mvn clean` 删除 target
* `mvn install` 安装jar包到本地仓库

### maven快速创建项目骨架目录 ###
* `mvn archetype:generate` 根据提示进行
* `mvn archetype:generate -DgroupId=组织名，公司网址反写-项目名  -DartifactId=项目名-模块名 -Dversion=版本号 -Dpackage=代码所在的包`
