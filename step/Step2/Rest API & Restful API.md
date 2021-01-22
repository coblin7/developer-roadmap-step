# REST(Representational State Transfer)

자원을 이름(자원의표현)으로 구분하여 해당 자원의 상태(정보)를 주고 받는 모든 것을 의미한다.

즉, 자원(resource)의 표현(representation)에 의한 상태 전달
a. 자원의 표현 :
- 자원 : 해당 소프트웨어가 관리하는 모든 것(예: 문서, 그림, 데이터, 해당 소프트웨어 자체 등)
- 자원의 표현 : 자원을 표현하기 위한 이름(예: DB의 학생 정보가 자원일 때, 'student'를 자원의 표현으로 정함)
b. 상태(정보) 전달 : 
- 데이터가 요청되어지는 시점에서 자원의 상태(정보)를 전달한다.
- JSON 혹은 XML을 통해 데이터를 주고 받는 것이 일반적이다.

REST는 기본적으로 웹의 기존 기술과 HTTP 프로토콜을 그대로 활용하기 때문에 웹의 장점을 최대한 활용할 수 있는 아키텍쳐 스타일이다.

REST는 네트워크 상에서 Client와 Server 사이의 통신 방식 중 하나이다.

웹에 있는 자원을 HTTP를 통하여 직관적으로 전달하기 위한 간단한 인터페이스이다.

RESTFUL API는 대부분의 데이터를 JSON 형식이나 XML 형식으로 담아서 HTTP 프로토콜 위에서 통신하는 API 이다.


# REST의 구체적인 개념

HTTP URI를 통해 자원을 명시하고 HTTP METHOD를(POST, GET, PUT, DELETE)를 통해 해당 자원에 대한 CRUD Operation을 적용하는 것을 의미한다.

즉, REST는 자원 기반의 구조(ROA, Resource Oriented Architecture) 설계의 중심에 Resource가 있고 HTTP Method를 통해 Resource를 처리하도록 설계된 아키텍쳐를 의미한다.

웹 사이트의 이미지, 텍스트, DB 내용 등의 모든 자원에 고유한 ID인 HTTP URI를 부여한다.

CRUD Operation :
- Create : 생성(POST)
- Read : 조회(GET)
- Update : 수정(PUT)
- Delete : 삭제(DELETE)
- HEAD : header 정보 조회(HEAD)

# RESTFUL

RESTFUL 하다는 것은 REST 법칙에 통과한 것을 말한다.
법칙은 아래와 같다.
1. 자원
2. 메소드(Method: GET, POST, PUT, DELETE)만으로 표현
3. 동사말고 명사만
4. 확장자는 포함하지 않음

즉, 'naldo'라는 사용자를 찾는 URL 메서드를 설계할 때, Restful 하다고 할 수 있는 예시는
/users/naldo (GET) 이 될 것이다.

Restful 메서드는 CRUD연산과 연결지어서 사용이 가능하다.

