# 스프링 부트 + Jsp

### 프로젝트 구성
* 자바 11
* boot 2.4.1
* lombok
* gradle 6.6

## 설명
 - 그레이들에 jsp를 사용하기 위한 라이브러리 의존성을 추가한다.
 
```gradle
providedRuntime 'org.apache.tomcat.embed:tomcat-embed-jasper'
implementation 'javax.servlet:jstl:1.2'
```

 - jsp파일은 webapp/WEB-INF에 위치한다.
 - application.yml에 jsp 파일 경로와 확장자 설정을 하고 자바스크립트와 같은 정적 리소스가 위치하는 경로를 설정해야한다.
    - 경로설정 방법 [링크](https://atoz-develop.tistory.com/entry/spring-boot-web-mvc-static-resources)
    - 정적 파일 다운로드는 다음 링크를 참조한다. [링크](https://programmer93.tistory.com/44)
 
```yml
spring:
  mvc:
    view:
      prefix: /WEB-INF/views/
      suffix: .jsp
    static-path-pattern: /resource/**
```
   
