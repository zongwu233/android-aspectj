# How to integrate with Maven #
To integrate with Maven you need to download / integrate aspectJ plugin in pom.xml
  * Changes to **pom.xml**

  1. Add AspectJ dependency to pom.xml.
```
	<dependency>
		<groupId>org.aspectj</groupId>
		<artifactId>aspectjrt</artifactId>
		<version>1.6.10</version>
        </dependency>
```
  1. Add Aspectj maven plugin to pom.xml.
```
	 <plugin>
                <groupId>org.codehaus.mojo</groupId>
                <artifactId>aspectj-maven-plugin</artifactId>
                <version>1.3.1</version>
                <executions>
			<execution>
				<goals>
					<goal>compile</goal>    <!-- use this goal to weave all your main classes -->
				</goals>
			</execution>
		</executions>
		<configuration>
			<complianceLevel>1.5</complianceLevel> <!-- set java code source level -->
		</configuration> 
	</plugin>
```
  * Where to put AspectJ code
> > Put AspectJ code in
```
src/main/aspect/Trace.aj
```
> > Sample [Trace.aj](http://code.google.com/p/android-aspectj/source/browse/src/com/test/Trace.aj) file.
  * Create jar with aspectJ
```
mvn aspectj:compile package install
```

> Above command will compile classes with help of aspectj and create a jar and install it in local repository.

# References #

[Apache Maven ](http://maven.apache.org/)


[AspectJ Maven plugin](http://maven.apache.org/maven-1.x/plugins/aspectj/)