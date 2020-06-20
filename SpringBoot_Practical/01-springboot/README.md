## SpringBoot实战派阅读笔记

这本书的实战性很强，并且基本上是面面俱到，阅读完第四章才开始做笔记。

### 进入SpringBoot世界

第一章进入springboot的世界主要讲的是Spring，SpringBoot和SpringCloud的关系，以及SpringBoot的一些特性。

介绍了Spring Boot的两大核心：

    - 约定大于配置：做到了零配置和极简配置
    - 起步依赖：提供starter，做到了快速配置和使用

依靠两大核心实现了开箱即用。

Spring依靠各个组件和模块来简化了基础构建，提高了开发效率，但仍需要额外配置。

Spring Boot是Spring的扩展和自动化，依赖于Spring，仅仅是消除了xml配置，简化了开发。

Spring Cloud依赖于Spring Boot，仅仅是一套分布式服务治理的框架，本身并不提供任何的功能性操作，只专注于服务间的
通信、熔断和监控等，利用各种组件开发微服务。

简单的来说： Spring是基础，SpringBoot依赖于Spring进行快速的构建和开发，Spring Cloud依赖于Spring Boot进行组件的整合，
来搭建微服务。这就是三者的关系。

Spring Boot的特色（核心+微服务）：
    
    - 配置简单（约定大于配置）：注解进一步简化开发
    - starter依赖： 进一步简化配置，只需要引入starter，提供了默认的配置（mysql那些配置除外）
    - 部署简单： 内置了容器
    - 监控简单： actuator可以检查服务状态，容器的内容等
    - 为微服务的构建提供了便利

### 准备开发环境

Java的安装和Maven的安装。

Java官网下载msi，手动安装，配置环境变量： JAVA_HOME和PATH

maven官网下载zip，进行解压，配置环境变量： MAVEN_HOME和PATH，配置conf文件，conf文件修改本地仓库存储位置和配置阿里云镜像。

还有对maven的pom.xml进行了解。

### 使用开发工具

IDEA，STS，Eclipse的使用，重点是IDEA的使用，更加简单智能。

### Spring Boot的基础

项目结构：

    - src/main/java： 业务开发
    - src/main/resource：配置文件和静态资源
    - src/test/java： 测试
  
热部署：引入spring-boot-devtools依赖就可使实现

定制启动画面： 直接在resource下放 banner.txt或者以banner为名的图片就可以。

常用的注解（很多，并且可以作用在各个地方，下面仅列举我常用的，不一一列举了）：

    - 作用于类上
        - @RestController
        - @Service
        - @Repository
        - @Component
        - @COnfiguration
        - @Transactional
    - 方法上
        - @Resource
        - @Autowried
        - @RequestMapping
        - @Bean
    - 属性上
        - @Resource
        - @Autowried
    - 方法参数前
        - @PathVariable
        - @RequestBody
    
配置文件： 支持properties和yaml两种，前者优先级高于后者

配置多环境： 需要有主配置文件，在主配置文件中指定环境，spring.profiles.active来指定。
     



