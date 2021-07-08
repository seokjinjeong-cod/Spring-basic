# 스프링의 핵심  
 - 스프링은 자바 언어 기반의 프레임워크  
 - 자바 언어의 가장 큰 특징 - 객체 지향 언어  
 - 스프링은 객체 지향 언어가 가진 강력한 특징을 살려내는 프레임워크  
 - 스프링은 좋은 객체 지향 어플리케이션을 개발할 수 있게 도와주는 프레임워크      

출처:https://www.inflearn.com/course/%EC%8A%A4%ED%94%84%EB%A7%81-%EC%9E%85%EB%AC%B8-%EC%8A%A4%ED%94%84%EB%A7%81%EB%B6%80%ED%8A%B8/  

## CURD란?  
CRUD는 존재하는 거의 대부분의 소프트웨어가 가지고있는 기본적인 데이터 처리 기능을 뜻한다.  
쉽게 말하면 로그인하고, 글을 올리고, 회원가입을 하고, 내가 찜한 목록을 삭제하는 등  
이러한 모든 데이터 관련 처리의 가장 기초를 뜻한다.  

 - ### Create
 - 데이터를 생성 또는 저장하는 기능
 - sql의 insert에 해당
 - ### Read
 - 저장된 데이터를 읽는 기능
 - sql의 select에 해당
 - ### Update
 - 저장된 데이터의 값을 새롭게 갱신하는 기능
 - sql의 update에 해당
 - ### Delete
 - 저장된 데이터를 삭제하는 기능
 - sql의 delete에 해당         


## MVC 패턴이란?  
MVC 패턴이란 Spring Framework에서 제공하는 웹 모듈이다.  
MVC는 Model, View, Controller의 약자이며, 시스템 모듈을  Model, View, Controller로 나누어서 구현되어있다.  
 - ### Model
 - 어플리케이션이 “무엇”을 할 것인지를 정의.  내부 비지니스 로직을 처리하기 위한 역할  
 - 처리되는 알고리즘, DB 와 상호작용(CRUD Create Read Update Delete), 데이터 등  
 - ### View
 - 화면에 “무엇” 인가를 보여주기 위한 역할
 - 컨트롤러 하위에 종속되어, 모델이나 컨트롤러가 보여주려고 하는 모든 필요한 것들을 보여준다.  
 - 사용자에게 “무엇”을 화면(UI)으로 보여준다
 - ### Controller
 - 모델이 “어떻게” 처리할 지를 알려주는 역할을 할 것이고, 모바일에서는 화면의 로직처리 부분
 - 화면에서 사용자의 요청을 받아서 처리되는 부분을 구현되게 되며, 요청 내용을 분석해서 Model과 View에 업데이트 요청
 - 사용자로 부터의 입력 을 받고 Model 또는 View 중개   

## 스프링 AOP(Aspect Oriented Programming)  
AOP는 Aspect Oriented Programming의 약자로 관점 지향 프로그래밍이라고 불린다.   
관점 지향은 쉽게 말해 어떤 로직을 기준으로 핵심적인 관점, 부가적인 관점으로 나누어서 보고 그 관점을 기준으로 각각 모듈화하겠다는 것이다.  
여기서 모듈화란 어떤 공통된 로직이나 기능을 하나의 단위로 묶는 것을 말한다.   
예로들어 핵심적인 관점은 결국 우리가 적용하고자 하는 핵심 비즈니스 로직이 된다.   
또한 부가적인 관점은 핵심 로직을 실행하기 위해서 행해지는 데이터베이스 연결, 로깅, 파일 입출력 등을 예로 들 수 있다.  
AOP에서 각 관점을 기준으로 로직을 모듈화한다는 것은 코드들을 부분적으로 나누어서 모듈화하겠다는 의미다.   
이때, 소스 코드상에서 다른 부분에 계속 반복해서 쓰는 코드들을 발견할 수 있는 데 이것을 흩어진 관심사 (Crosscutting Concerns)라 부른다. 
  
![image](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=http%3A%2F%2Fcfile26.uf.tistory.com%2Fimage%2F994AA3335C1B8C9D28D24B)   

위와 같이 흩어진 관심사를 Aspect로 모듈화하고 핵심적인 비즈니스 로직에서 분리하여 재사용하겠다는 것이 AOP의 취지다.   

출처: https://engkimbs.tistory.com/746?category=767795  

## Spring-Data-JPA(Java Persistence API)란?  
ORM은 "관계형 데이터베이스의 구조화된 데이터와 자바와 같은 객체 지향 언어 간의 구조적 불일치를   
어떻게 해소할 수 있을까"라는 질문에서 나온 객체-관계 매핑 프레임워크이다. 즉, 객체와 릴레이션을   
매핑할 때 생기는 다양한 문제들을 해결할 수 있는 솔루션이라 생각하면 된다.
JPA은 ORM을 위한 자바 EE 표준이며 Spring-Data-JPA는 JPA를 쉽게 사용하기 위해 스프링에서 제공하고 있는 프레임워크이다.
추상화 정도는 Spring-Data-JPA -> JPA -> Hibernate -> Datasource (왼쪽에서 오른쪽으로 갈수록 구체화) 이다.
참고로, Hibernate는 ORM 프레임워크이며 DataSource는 스프링과 연결된 MySQL, PostgreSQL 같은 DB를 연결한 인터페이스이다.  


출처: https://engkimbs.tistory.com/790 [새로비]
