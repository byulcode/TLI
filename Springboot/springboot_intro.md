# 1. 스프링 부트 시작하기

---

### 00. 스프링 프레임워크란?

---

- 스프링은 자바 애플리케이션 개발에 사용되는 오픈소스 프레임워크다.
- 자바 객체의 생성, 소멸 등의 라이프사이클을 관리하고 언제든 필요한 객체를 가져와 사용할 수 있다.
- 스프링 프레임워크의 핵심 기능은 IoC(Inversion of Control : 제어 역전), DI(Dependency Injection : 의존성 주입) 이다.
  - IoC : Singleton으로 bean을 관리하는 Container. 객체의 조작을 스프링 프레임워크에 위임하고 개발자는 의존성 객체의 메소드를 호출한다.
  - DI : 객체 생성 시 직접적으로 생성하지 않고 외부(Ioc컨테이너)에서 생성한 후 주입하는 방법. → 모듈 간의 결합도 느슨해져 유연성이 높아진다.

### 01. 스프링 부트 소개

---

- [스프링 부트 공식문서](https://docs.spring.io/spring-boot/docs/2.0.3.RELEASE/reference/htmlsingle/#getting-started-introducing-spring-boot)
-
