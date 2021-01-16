# 개요
라우저는 HTTP 메시지 생성 후 도메인 이름의 IP주소를 조사한다. <br/>
이는 HTTP 메시지를 만든 후 전송할 주소를 알아야 하기 때문에 IP주소 조회를 OS에 의뢰하게 된다.

# DNS(Domain Name System)
DNS는 사람들에게는 쉽게 기억될 수 있게 도입되었으나, 왜 IP주소가 아닌 문자로 주소를 주고 받을 수 없는가에 대한 의문을 남기곤 한다.
문자는 byte의 크기가 IP주소보다 크기 때문에 라우터에 과부하를 주어 처리를 지연되게 한다.

# DNS와 Resolver
DNS 또한 IP주소를 조회하기 위해 DNS 서버에 접근해야 하는데, DNS 클라이언트는 Resovler라고 한다. <br/>
DNS 원리를 사용해 IP주소를 조회하는 것은 Name Resolution이라고 한다. <br/>
Resolver는 이 Resolution을 실행한다. <br/>
Resolver는 OS의 Socket 라이브러리에 포함되어 있다. Socket라이브러리는 네트워크 기능을 호출하기 네트워크용 표준 라이브러리이다. <br/>
Resolver를 통해 DNS 서버에 해당 주소를 조회 후 응답메시지를 받고 메시지 안에 주소를 브라우저의 메모리 영역에 넣는다. <br/>

**도메인명에서 ip주소를 조회할 때 Socket 라이브러리의 Resolver를 이용한다.**

송신 동작은 Resolver가 스스로 실행되는 것이 아닌 OS의 프로토콜 스택을 통해 이루어진다. <br/>
Resolver는 OS 동작을 호출하기 위한 수단일 뿐 송수신 기능이 없기 때문이다.





