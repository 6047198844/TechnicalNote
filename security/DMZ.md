# **비무장지대(DMZ)**

## 작성자
[![Stupid07](https://avatars1.githubusercontent.com/u/35564566?s=100&v=4)](https://github.com/Stupid07)

## 회사에서 듣게 될 단어

- 보안을 위해 내부망을 구축하고 있는 회사에 들어가면 종종 "DMZ"라는 단어를 듣게 된다.

  > **DMZ구간**에 있는 파일 중에 보안에 취약한 파일이나 중요정보가 남지 않도록 주의해야...

- 처음 듣는 용어라면 머리속에 **?** 가 떠오를 것이다.

- ~~내부망이면 내부망이고 외부망이면 외부망이지 이놈의 IT는 뭔 용어가 이렇게 많을까?~~

- 그리고 회사 선배에게 "**DMZ가 뭐에요? 우리나라와 북한 사이에 있는 비무장지대?**" 라고 묻는다면 회사 생활이 더 재밌어 질테니 이 글을 통해 무슨 용어인지 알아 봅시다.



## 비무장지대(DMZ) 이란?

- 네트워크에서의 **Demilitarized zone**(**DMZ**)는 내부망과 외부망 사이에 존재하는 영역을 말한다.
- 공유기 처럼 공인 IP 주소를 내부 네트워크에서 활용하기 위해서 내부망을 구축할 수 있지만, 대부분의 내부망은 보안 때문에 구축한다.
- 이 때, 구축한 내부망에서 서비스를 제공하거나, 제공받기 위해 외부망과 연결이 필요할 수 있다.
- 하지만 내부망과 외부망을 단순히 방화벽 하나만 믿고 직접 연결하기엔 외부에서 내부망의 접속 경로(IP, PORT)를 알기에 구축한 내부망이 보안에 취약해진다.
- 이 때, 내부망과 외부망의 중간 지점인 DMZ 구간을 만들고, 외부망은 DMZ로만, 내부망도 DMZ로만 통신하면서 외부에서 내부망의 접속 경로를 모르도록 설계한 영역이 DMZ이다.
- 이 DMZ는 물리적으로 외부망-DMZ-내부망 형태로 존재할 수도 있고, VLAN 등을 활용해 논리적으로 존재하는 가상의 형태로도 가능하다.

### 장점

- 외부망에서 내부망으로 직접 연결할 경로를 찾기 힘들다.
- 중계 서버 형태로 웹 서버를 올려놓으면 프록시 서버처럼 정적 컨텐츠를 내부망을 거치지 않고 응답 가능하다.
- 외부망과 DMZ 사이, DMZ와 내부망 사이의 방화벽을 분리하여 하나의 방화벽이 무너져도 바로 침투하기 힘들다.

### 단점

- 결국 DMZ는 내부망과 연결되어 있기에 DMZ가 장악당하면 DMZ를 경유해 내부망에 침투할 수 있다.
- DMZ 구간을 구축하더라도 DMZ 내부에 중요 정보들이 남지 않도록 관리하지 않는다면 오히려 보안 취약점이 될 수 있다.



## 참조

- [비무장지대 (컴퓨팅)](https://ko.wikipedia.org/wiki/%EB%B9%84%EB%AC%B4%EC%9E%A5%EC%A7%80%EB%8C%80_(%EC%BB%B4%ED%93%A8%ED%8C%85))
- [네트워크에도 ‘비무장지대(DMZ)’가 있다?](https://www.boannews.com/media/view.asp?idx=81495)
