### Contents

> * JUnit
> * TDD



### JUnit

---

* 자바 프로그래밍 언어용 단위 테스트 프레임워크 - [단위 테스트 작성 이유](https://docs.microsoft.com/ko-kr/dotnet/core/testing/unit-testing-best-practices)
* 테스트 결과는 **테스트 클래스**로 작성하여 개발자에게 테스트 방법 및 클래스의 히스토리를 남기고 공유가 가능
* **단정(Assert) 메서드**로 테스트 케이스의 수행 결과를 판별
* **어노테이션(Annotation)**으로 간결하게 지원(JUnit4 부터)



#### JUnit4와 JUnit5

|                            |    JUnit4    |                     JUnit5                     |
| :------------------------: | :----------: | :--------------------------------------------: |
| **Supported Java Version** | Java 5 이상  |                  Java 8 이상                   |
|      **Architecture**      |  All in one  | JUnit Platform + JUnit Jupiter + JUnit Vintage |
|       **Assertions**       | Assert Class |                Assertion class                 |



### 기본 어노테이션

---

* **@Test (JUnit4 & JUnit5)**
  * 테스트를 만드는 모듈 역할. 어노테이션이 있는 메소드는 클래스의 테스트 케이스를 나타냄

* **@Before (JUnit4) / @BeforeEach (JUnit5)**
  * 테스트 클래스의 각 테스트 메서드를 실행하기 전에 실행
  * 각 테스트를 시작하기 직전에 리소스 또는 테스트 데이터를 설정하려는 경우에 사용

* **@After (JUnit4) / @AfterEach (JUnit5)**
  * 테스트 클래스의 각 테스트 메서드가 실행 된 후에 실행
  * 각 테스트가 실행된 후 사용 된 리소스 또는 테스트 데이터를 해제해야 할 때 사용

* **@BeforeClass (JUnit4) / @BeforeAll (JUnit5)**
  * 테스트 클래스의 모든 테스트 메서드가 실행되기 전에 실행
  * 리소스를 설정학거나 클래스 수준에서 데이터를 테스트하려는 경우에 사용
  * 메서드는 정적으로 지정 되어야 함

* **@AfterClass (JUnit4) / @AfterAll (JUnit5)**
  * 테스트 클래스의 모든 테스트 메서드가 실행된 후에 실행
  * 사용 된 리소스 또는 테스트 데이터를 클래스 수준에서 해제하려는 경우에 사용
  * 메서드는 정적으로 지정 되어야 함

* **@Ignore (JUnit4) / @Disable (JUnit5)**
  * 테스트 클래스 또는 메서드를 비활성화



#### 단정 메서드 [[더보기]](http://junit.sourceforge.net/javadoc/org/junit/Assert.html) --> 더 추가!

---

- **assertArrayEquals(a, b)**
  : 배열 A와 B가 일치함을 확인
- **assertEquals(a, b)**
  : 객체 A와 B가 같은 값을 가지는지 확인
- **assertEquals(a, b, c)**
  : 객체 A와 B가 값이 일치함을 확인( a: 예상값, b:결과값, c: 오차범위)
- **assertSame(a, b)**
  : 객체 A와 B가 같은 객체임을 확인
- **assertTrue(a)**
  : 조건 A가 참인지 확인
- **assertNotNull(a)**
  : 객체 A가 null이 아님을 확인