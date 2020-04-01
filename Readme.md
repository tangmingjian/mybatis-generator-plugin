### mybatis generator 插件
    * LombokPlugin 类加Lombok注解
    * MyCommentGenerator 字端添加Comment

1. pom中添加mybatis generator插件
```xml
<build>
        <plugins>
            <plugin>
                <groupId>org.mybatis.generator</groupId>
                <artifactId>mybatis-generator-maven-plugin</artifactId>
                <version>1.3.7</version>
                <configuration>
                    <configurationFile>${basedir}/src/test/resources/generatorConfig.xml</configurationFile>
                    <overwrite>true</overwrite>
                    <verbose>true</verbose>
                </configuration>
                <dependencies>
                    <dependency>
                        <groupId>com.gpay.mybatis.generator</groupId>
                        <artifactId>mybatis-plugin</artifactId>
                        <version>1.0.0-SNAPSHOT</version>
                        <scope>system</scope>
                        <systemPath>${basedir}/src/test/lib/mybatis-plugin-1.0.0-SNAPSHOT.jar</systemPath>
                    </dependency>
                    <dependency>
                        <groupId>oracle.ojdbc</groupId>
                        <artifactId>ojdbc6</artifactId>
                        <version>11.2.0.4.0</version>
                    </dependency>
                </dependencies>
            </plugin>
        </plugins>
    </build>

```
2. [配置generatorConfig.xml](./src/test/resources/generatorConfig.xml)