# spring-data-jpa
About spring-data-jpa

## Spring Data JPA

JPA란 영속성을 위한 API이다. 이것 자체가 스프링의 것은 아니고, JAVA SE/EE에서 준비된 기능이다. 데이터를 보존하고 영속적으로 이용 할 수 있도록 하기 위한 틀이라고 생각하면 된다. 또한 JPA는 ORM의 기능도 제공하고 있다. ORM 이란 Object Relational Mapping의 준말로 관계형 데이터베이스의 데이터를 JAVA의 오브젝트에 맵핑하기 위한 시스템이다. 이것에 의해 JAVA의 오브젝트와 같은 감각으로 데이터 베이스의 레코드를 다룰 수 있게 된다. 이렇게 JPA를 스프링 환경에서 이용하기 위한 프레임워크가 Spring Data JPA라고 할 수 있다.

## Spring Data JPA이용에 필요한 것들

- Spring Data JPA 라이브러리

      ` <dependency> `<br>
           `<groupId>org.springframework.data</groupId>`<br>
           `<artifactId>spring-data-jpa</artifactId>`<br>
           `<version>${spring-version}</version>`<br>
       `</dependency>`
      
- Entity Class 파일

  - Entity란?
  
      JPA에서 다루는 데이터를 보관하기 위한 오브젝트를 말한다. 데이터베이스에서는 각 테이블에 레코드로서 데이터를 보관하지만, JPA에서는 이 레코드에 상당하는 것들을 Entity라고 불리는 Class로서 다룬다. 이 Entity에는 데이터 뿐만 아닌, 그 Entity를 처리하기 위한 기능 등도 구현된다.
  
  - Entity를 위한 어노테이션들
   
      `@Entity`

      `@Table(name="이름")`
      
      `@Id`
      
      `@Column(name=이름, length=길이, nullable=false)`
      
      `@GeneratedValue(strategy = GenerationType.AUTO)`
      
       
- persistence.xml 파일

  - Persistence Unit이란?
   
    JPA에서는 "영속성 유닛"이라고 불리는 것을 사용한다. 이것은 자체에서 작성되는것이 아닌, 라이브러리등에 포함되어 제공되고 있는 것으로 이용한다. 어플리케이션에서 이용하는 영속성 유닛의 정의를 기술한 것이 "persistence.xml" 이 되겠다.

  - persistence.xml 작성법
   
    `src/main/resources/META-INFO`에 위치

    

- Bean 구성 파일

- Property 파일

- Application Class 파일

## Entity
