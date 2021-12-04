# 회원 관리 서비스를 통한 웹 MVC 개발

### Project Settings
 - Gradle Project
 - Java 11
 - Jar
 - Spring Boot 2.5.4
 - Dependencies
   - Spring Web
   - Thymeleaf



### Build & Execute
```
$ ./gradlew clean build
$ cd build/libs
$ java -jar hello-spring.jar
```


### Libraries
Gradle은 의존 관계가 잇는 라이브러리를 함께 다운로드 한다.
1. Spring Boot Library 
   - spring-boot-starter-web
     - spring-boot-starter-tomcat (Web Server)
     - spring-webmvc 
   - spring-boot-starter-thymeleaf (Template Engine)
   - spring-boot-starter(common : spring boot + spring core + logging)  
     - spring-boot
       - spring-core
     - spring-boot-starter-logging
       - logback, slf4j

2. Test Library
   - junit
   - mockito
   - assertj 
   - spring-test 


### Web Development 
- Static contents
    - resources/staic/hello-static.html
    - http://localhost:8080/hello-static.html 
- MVC pattern and template engine
     ```
    @GetMapping("hello-mvc")
    public String helloMvc(@RequestParam("name") String name, Model model) {
        model.addAttribute("name", name);
        return "hello-template";
    }
     ```
  - resources/template/hello-template.html
  - ViewResolver 
  - http://localhost:8080/hello-mvc?name=spring
- API
    ```
    @GetMapping("hello-string")
    @ResponseBody
    public String helloString(@RequestParam("name") String name) {
        return "hello " + name;
    }
    ```
  - HttpMessageconverter 
  - http://localhost:8080/hello-string?name=spring


### Member Board Service 



### Spring Bean and Dependency




### Database 


### AOP 

