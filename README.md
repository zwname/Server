1.安装lombok
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
2、CommandLineRunner接口 
	实现后@Order(num)指定加载顺序
3、banner.txt文件可以对运行时的标志进行修改

4.日志log4j
		日志级别：trace debug info warn error fatal 默认info
		
		
5.添加server依赖，可作为一个被访问的服务器，监听访问者信息
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