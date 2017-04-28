# mybatis-generator-demo

使用Mybatis-Generator自动生成Dao、Model、Mapping相关文件

1.自动生成的代码 可自定义注释根据 根据org.mybatis.generator.internal.DefaultCommentGenerator 实现
实现类：org.mybatis.generator.GenCommentGenerator

2.中启动方式
1. maven 插件形式
    mvn mybatis-generator:generate
    根据generatorConfig.xml 生成
    配置文件 generatorConfig.properties 
        可配置数据源，生成代码位置(相对路径，或绝对路径)

    jdbc的jar 需要在 POM mybatis-generator-maven-plugin 插件中的dependencies 引入jar
    或者通过
    配置文件 dirverJar 配置jdbc驱动包的绝对路径
    

2. java main 方式启动
源码：org.mybatis.generator.StartUp.main
    根据generatorConfig-java.xml 生成
    配置文件 generatorConfig-java.properties
        可配置数据源，生成代码位置(绝对路径)

    jdbc的jar 需要在 POM dependencies中引入
   