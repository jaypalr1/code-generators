# code-generators

## WSDL to Java

Generate Java classes from WSDL files

### WSDL

* Used mostly for specifying soap requests just like swagger specification.

### References

* [Baeldung](https://www.baeldung.com/maven-wsdl-stubs)
* [Spring](https://spring.io/guides/gs/consuming-web-service)
* [HowToDoInJava](https://howtodoinjava.com/spring-boot/spring-boot-soap-webservice-example)
* [SpringBootTutorial](https://www.springboottutorial.com/creating-soap-web-service-with-spring-boot-web-services-starter)
* [Gradle](https://simplesolution.dev/gradle-configuration-to-generate-java-classes-from-wsdl-with-jaxb)

### Understanding

* Two dependencies need to be added as support for 'jaxws' was removed from JDK 11.
    1. org.glassfish.main.javaee-api:javax.jws:3.1.2.2
    2. javax.xml.ws:jaxws-api:2.3.1
* Add plugin <b> org.codehaus.mojo:jaxws-maven-plugin:2.6 </b> refer POM and run command <b> mvn
  clean install. </b>
* Running <i> mvn install </i> will generate the required classes/stubs.
* In this project I've used <i> WSDL </i> with <i> MapStruct </i>.

### find out more:

* [GoogleSearch](https://www.google.com/search?q=maven-jaxb2-plugin+vs+jaxws-maven-plugin&rlz=1C1GCEA_enIN1004IN1004&sxsrf=ALiCzsZ2d05sbwzVZx-pobmpFWNe7AiWaQ%3A1658124215991&ei=t_fUYuCPPPWTz7sP1fOqiAY&oq=maven-jaxb2-plugin+vs+jaxws&gs_lcp=Cgdnd3Mtd2l6EAMYATIGCAAQHhAWMgYIABAeEBYyBQgAEIYDMgUIABCGAzoHCAAQRxCwAzoFCAAQgARKBAhBGABKBAhGGABQkQVYvAhgqRxoAXABeACAAaUBiAHlA5IBAzAuM5gBAKABAcgBCMABAQ&sclient=gws-wiz)

## XSD to Java

Generate Java classes from XSD files

### XSD:

It stands for XML(Extensible Markup Language. A markup language similar to HTML, but without
predefined tags to use) Schema Definition

### Reference:

[Code Journal](https://www.thecodejournal.tech/2020/12/generating-code-using-maven-xsd-to-java/)

### Understanding

* Add two dependencies:
  * jaxb-api
  * jaxb-impl
* Add plugin as shown in the code:
  * org.codehaus.mojo:jaxb2-maven-plugin:3.1.0