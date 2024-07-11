## Section1


<h3>인터넷 통신</h3>
클라이언트는 인터넷 망을 거쳐서 서버와 통신한다.

<h3>인터넷 프로토콜(IP)</h3>
<ul>
  <li>인터넷 프로토콜 역할</li>
    <ul>
      <li>
        지정한 IP주소로 데이터를 전달
      </li>
      <li>
        패킷이라는 통신 단위로 데이터를 전달
      </li>
    </ul>
</ul>

<h3>IP 패킷</h3>
패킷에는 출발지 IP, 목적지 IP ..등이 있고 전송 데이터가 담겨져 있다.

<h3>IP 프로토콜의 한계</h3>
<ul>
  <li>비연결성</li>
  <ul>
  <li>패킷를 보낼 대상이 없거나 서비스가 불능인 상태여도 패킷을 전송한다.</li>
  </ul>
  <li>비신뢰성</li>
  <ul>
    <li>중간에 패킷이 사라지거나 순서대로 안올시</li>
    <blockquote>패킷이 전송 도중에 유실되면 클라이언트는 전송이 성공적으로 되었는지 모른다..</blockquote>
  </ul>
  <li>프로그램 구분</li>
  <ul>
    <li>
      같은 IP를 사용하는 서버에서 통신하는 애플리케이션이 둘 이상이라면?
    </li>
  </ul>
</ul>


<h3>인터넷 프로토콜 스택의 4계층</h3>
<ul>
  <li>애플리케이션 계층 - HTTP, FTP</li>
  <li>전송 계층 - TCP, UDP</li>
  <li>인터넷 계층 - IP</li>
  <li>네트워크 인터페이스 계층</li>
</ul>

<h3>TCP/IP 패킷 정보</h3>
IP 패킷 [출발지 IP, 목적지 IP, 기타...] <br>
TCP 세그먼트 [출발지 PORT, 목적지 PORT, 전송 제어, 순서, 검증 정보...]<br><br>

[애플리케이션 계층]게임 채팅 프로그램이 Hello, world! 메시지 생성 (socket 라이브러리를 통해 os 계층으로 전달) -><br>[OS 계층]TCP 정보 생성, 메시지 데이터 포함 -> IP 패킷 생성, TCP 데이터 포함 -><br>[네트워크 인터페이스 계층]LAN 드라이버 LAN 장비 -> Ethernet Frame에 씌어져서 나감

<h3>TCP 특징</h3>
전송 제어 프로토콜(Transmission Control Protocal)

<ul>
  <li>
    연결지향 - TCP 3 way handShake (가상 연결)
  </li>
  <li>
    데이터 전달 보증
  </li>
  <li>
    순서 보장
  </li>
</ul>
