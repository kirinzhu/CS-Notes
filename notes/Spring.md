# Spring
<!-- GFM-TOC -->

* [Spring](#springl)
    
    * [1.spring 中都用到了哪些设计模式?](#design model)
    
    * [2.spring 中有哪些核心模块?](#core module)
    
    * [3.说一下你理解的 IOC 是什么?](#ioc)
    
    * [4.spring 中的 IOC 容器有哪些?有什么区别?](different ioc)
    
    * [5.那 BeanFactory 和 FactoryBean 又有什么区别?](#different beanfactory)
    
    * [6.@Repository、@Service、@Compent、@Controller它们有什么区别?](#different comment)
    
    * [7.@Autowired 和 @Resource 有什么区别?](#different 3)
    
    * [8.说说 AOP 是什么?](#AOP)
    
    * [9.Spring AOP 和 AspectJ AOP 有什么区别？](#different aop)
    
    * [10.动态代理和静态代理有什么区别?](#proxy 1)
    
    * [11.JDK 动态代理和 CGLIB 代理有什么区别？](#proxy 2)
    
    * [12.spring 中 Bean 的生命周期是怎样的?](#bean life)
    
    * [3.那么依赖注入 DI 又是什么?](#DI 1)
    
    * [14.spring 是怎么解决循环依赖的?](#DI 2)
    
    * [15.为什么要使用三级缓存，二级缓存不能解决吗?](#DI 3)
    
    * [16.spring 事务隔离级别有哪些?](#commit 1)
    
    * [17.spring 事务的传播机制有哪些?](#commit 2)
    
    * [18.springBoot 自动装配原理?](#auto bean)
    
        <!-- GFM-TOC -->


## 1.spring 中都用到了哪些设计模式?

「1.工厂设计模式」: 比如通过 BeanFactory 和 ApplicationContext 来生产 Bean 对象
「2.代理设计模式」:  AOP 的实现方式就是通过代理来实现，Spring主要是使用 JDK 动态代理和 CGLIB 代理
「3.单例设计模式」: Spring 中的 Bean 默认都是单例的
「4.模板方法模式」: Spring 中 jdbcTemplate 等以 Template 结尾的对数据库操作的类，都会使用到模板方法设计模式，一些通用的功能
「5.包装器设计模式」: 我们的项目需要连接多个数据库，而且不同的客户在每次访问中根据需要会去访问不同的数据库。这种模式让我们可以根据客户的需求能够动态切换不同的数据源
「6.观察者模式」: Spring 事件驱动模型观察者模式的
「7.适配器模式」:Spring AOP 的增强或通知(Advice)使用到了适配器模式

![Picture1](/Users/zlx/Downloads/interview/pictures/Picture1.png)



## 2.spring 中有哪些核心模块?

- 1.**「****Spring Core****」**：Spring核心，它是框架最基础的部分，提供IOC和依赖注入DI特性
- 2.**「****Spring Context****」**：Spring上下文容器，它是 BeanFactory 功能加强的一个子接口
- 3.**「****Spring Web****」**：它提供Web应用开发的支持
- 4.**「****Spring MVC****」**：它针对Web应用中MVC思想的实现
- 5.**「****Spring DAO****」**：提供对JDBC抽象层，简化了JDBC编码，同时，编码更具有健壮性
- 6.**「****Spring ORM****」**：它支持用于流行的ORM框架的整合，比如：Spring + Hibernate、Spring + iBatis、Spring + JDO的整合等
- 7.**「****Spring AOP****」**：即面向切面编程，它提供了与AOP联盟兼容的编程实现

![Picture1](/Users/zlx/Downloads/interview/pictures/Picture1.png)

