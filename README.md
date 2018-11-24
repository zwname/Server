1.配置对实体类属性赋值

		1.实体类添加@Configuration	@ConfigurationProperties(prefix = "前缀名")
		2.配置类中根据前缀名.属性=xx进行赋值
		3.在@Controller和@RestController的类中，@AutoWired实体类，使用实体类对象的方法进行输出。
		4.配置类的常用配置：以properties为例
			端口号：server.port=8088 
			项目名：server.context-path=/sample
			实体类属性：student.name=aaa 
				注意：
					1.该实体类必须有注解@Configuration	@ConfigurationProperties(prefix = "student")
					2.该实体类必须有属性的setting和getting方法
		5.配置类以application-环境.properties/yml命名，在指定的环境运行使用spring.profiles.active=环境名，有冲突则取优先级高的，没有则互补
		6.非application-环境.properties/yml的配置，可以在实体类中@PropertySource(value="classpath:test.properties")指定使用该配置中对实体类属性的赋值

2.安装lombok

      常用注解
	@Data：注解在类上；提供类所有属性的getting和setting方法，此外还提供   了equals、canEqual、hashCode、toString方法
	@Setter：注解在属性上；为属性提供setting方法
	@Getter：注解在属性上；为属性提供getting方法
	@Log4j：注解在类上；为类提供一个属性名为log的log4j日志对象
	@NoArgsConstructor：注解在类上；为类提供一个无参的构造方法
	@AllArgsConstructor：注解在类上；为类提供一个全参的构造方法
	
    注入依赖
		<dependency>
			<groupId>org.projectlombok</groupId>
			<artifactId>lombok</artifactId>
			<version>1.16.20</version>
		</dependency>	
3、CommandLineRunner接口 

	实现后@Order(num)指定加载顺序
4、banner.txt文件可以对运行时的标志进行修改

5.日志log4j

		日志级别：trace debug info warn error fatal 默认info
		
		
6.添加server依赖，可作为一个被访问的服务器，监听访问者信息

     <!--引入admin server依赖-->
        <dependency>
            <groupId>de.codecentric</groupId>
            <artifactId>spring-boot-admin-server</artifactId>
            <version>1.5.6</version>
        </dependency>
        <!--admin server的展示-->
        <dependency>
            <groupId>de.codecentric</groupId>
            <artifactId>spring-boot-admin-server-ui</artifactId>
            <version>1.5.6</version>
        </dependency>