# ch_07 네트워크 보안 기술

### 인증 : 접속하는 사용자와 기기를 제한하는 3가지 방법

##### 누가 접속했는가?

> 네트워크에 아무나 무제한으로 접속시킬 수는 없습니다. 접속 대상을 제한하려면, 네트워크에 접속하는 사용자와 기기를 제대로 확인할 필요가 있다. 확인을 위해서는 <strong>인증</strong>이란 방법을 사용한다.

##### 인증의 개용

> 인증이란 네트워크와 시스템을 이용하는 사용자 또는 기기가 정식으로 등록됐는지 확인하는 절차입니다. 인증을 통해 정식 사용자 이외에는 네트워크나 시스템에 접근할 수 없게 한다. 인증은 보안 대책에서 가능한 기본적이고 중요한 수단이다.
>
> <img src="https://ifh.cc/g/qxeFs4.jpg" alt="l3-switch" style="zoom:30%;" />
>
> 일반적으로 <strong>패스워드 인증</strong>을 사용한다. 또한 IC 카드 등 해당 사용자만 가진 <strong>물건으로 인증</strong>하는 방법이 있다. 그리고 사용자 신체적 특징을 이용한 인증이 있다. 신체의 특징을 이용하는 인증을 <strong>바이오메트릭스 인증</strong>이라고도 부른다.

### 암호화 : 데이터 도청을 방지하는 기술

##### 제3자에게 데이터가 유출될 위험성이 있다

> 네트워크 상에서 전송되는 데이터는 제3자에게 도청(유출)될 위험이 있다. 
>
> 데이터 도청을 방지하기 위해서는 데이터를 <strong>암호화</strong>할 필요가 있다.

##### 데이터 암호화

> 데이터를 암호화함으로써 정식 사용자 이외에는 그 데이터의 내용을 판별할 수 없게 한다.
>
> 암호화하기 전의 데이터를 <strong>평문</strong>이라고 부른다. 평문을 암호화 하기 위해서 <strong>암호키</strong>를 이용한다. 암호화란 평문과 암호키로 수학적 연산을 거쳐 암호화된 데이터인 <strong>암호문</strong>을 생성하는 것을 뜻한다.

##### 데이터 복호

> 암호문과 암호키를 이용해 암호와는 반대로 연선하면 원래 평문이 된다.
>
>  암호화된 것을 원래 평문으로 되돌리는 조작을 <strong>복호</strong>라고 부른다.
>
> 암호화 및 복호화를 할 때의 수학적 연산을 <strong>암호화 알고리즘</strong>으로 불린다.

<img src="https://ifh.cc/g/xxkG7Z.jpg" alt="l3-switch" style="zoom:30%;" />

### 공통키 암호 방식 : 키 하나로 데이터를 관리한다

##### 공통키 암호 방식

> <strong>공통키 암호 방식</strong>이란 암호화와 복호와에 같은 키를 이용하는 암호화 방식이다. 공통키 암호 방식은 <strong>대칭키 암호방식</strong>과 <strong>비밀키 암호방식</strong> 등으로 불린다.
>
> 공통키 암호 방식은 데이터의 암호화와 복호의 처리 부하가 작다는 장점이 있다.
>
> 반면에, 암호키의 공유가 어렵다는 커다란 단점이 있다. 어떻게 암호키를 안전하게 송신자와 수신자가 공유하는지가 공통키 암호 방식의 가장 중요한 과제이다.
>
> <img src="https://ifh.cc/g/WnIU2V.jpg" alt="l3-switch" style="zoom:30%;" />

##### 키 배송 문제

> 암호 해독의 가장 좋은 단서는 규칙성이다. 같은 암호키를 계속 사용하면, 암호 데이터의 규칙성에서 암호가 해독될 위험이 커진다. 즉, 암호키를 정기적으로 갱신할 필요가 있다.
>
> 데이터 송신자와 수신자 사이에서 어떻게 암호키를 공유하고 갱신하는지를 가리켜 <strong>키 배송 문제</strong>라고 한다.

##### 공통 암호 방식의 알고리즘

> 주요 공통키 암호 방식의 알고리즘으로는 <strong>3DES</strong>와 <strong>AES</strong>가 있다.

### 공개키 암호방식 : 2개의 키로 데이터를 관리한다

##### 암호화와 복호에 다른 키를 사용한다

> 공통키 암호 방식에서는 키 배송이 큰 문제이다. 그 문제를 해결하는 획기적인 암호화 방식이 <strong>공개키 암호 방식</strong>이다.
>
> 공개키 암호 방식에서는 우선 암호키 쌍을 만들어야 한다. 암호키 쌍은 일반적으로 공개키와 비밀키로 불린다. <strong>공개키</strong>와<strong>비밀키</strong>에는 수학적인 연관성이 있다.
>
> 따라서, 공개키는 공개해도 상관없지만, 비밀키는 제3자에게 알려지지 않도록 엄중히 관리해야 한다. 

##### 공개키로 암호화

> 데이터를 암호화해 송신할 경우, 송신자(클라이언트)는 수신자(서버)가 공개한 공개키를 입수한다. 그리고, 그 공개키로 데이터를 암호화해서 전송한다. 수신자(서버)는 비밀키로 암호 데이터를 복호화한다.
>
> 공개키로 데이터를 암호화한다는 것은 '누구나 암호화할 수 있다'는 것이다. 누구나 암호화할 수 있지만, 복호할 수 있는 것은 비밀키를 가진 사용자뿐이다.
>
> <img src="https://ifh.cc/g/WaloNz.jpg" alt="l3-switch" style="zoom:30%;" />



### 비밀키, RSA 암호, 타원곡선 암호 : 암호화된 데이터로 암호화한 상대를 특정한다

##### 비밀키로도 암호화할 수 있다

> 공개키 암호 방식을 설명할 때 앞에서 말한 '공개키로 암호화하고 비밀키로 복호한다'만 다루는 경우가 자주 있다. 하지만 비밀키로 암호화하고 공개키로 복호할 수도 있다.
>
> 비밀키로 암호화한 데이터를 공개키로 복호할 수 있다는 것은 데이터를 암호화한 사용자가 공개키에 대응하는 비밀키를 가지고 있다는 말이 된다.
>
> 암호화된 데이터를 수신한 사용자B가 사용자A의 공개키로 복호할 수 있다. 공개키로 복호할 수 있는 것은 비밀키로 암호화한 경우이다. 사용자B는 데이터를 암호화해서 전송한 사람이 사용자 A라는 것을 확인할 수 있다

<img src="https://ifh.cc/g/9RsaOs.jpg" alt="l3-switch" style="zoom:30%;" />



##### 공개키 암호 방식의 알고리즘

> 공개키 암호 방식의 알고리즘은 <strong>RSA 암호</strong>와 <strong>타원곡선 암호</strong>의 두 가지가 자주 이용된다. 
>
> RSA 암호는 매우 큰 수의 소인수 분해가 어렵다는 점에 바탕을 두고, 공개키와 비밀키 쌍을 생성해 암호 데이터를 연산하는 알고리즘이다.
>
> 타원곡선 암호는 타원곡선 상의 이산대수문제가 어렵다는 점에 바탕을 두고 공개키와 비밀키 쌍을 생성해 암호 데이터를 연산하는 알고리즘이다.



### 디지털 서명 : 데이터를 만든 상대방을 특정한다

##### 디지털 서명

> 비밀키로 암호화한 데이터는 공개키로 복호할 수 있는 원리를 이요하여, 데이터를 보낸 곳과 데이터가 변조되지 않았음을 확인하기 위해 <strong>디지털 서명</strong>이 있다.
>
> 데이터 보낼 때 서명용 데이터를 추가해서 전송한다. 수신하는 쪽에서 서명 데이터를 체크하면, 데이터가 변조되지 않았으며 보낸 사람이 누구인지 명확해진다.
>
> 구체적인 디지털 서명의 내용은 데이터의 <strong>해시값</strong>을 비밀키로 암호화한 것이다.

##### 디지털 서명의 원리

> 데이터를 전송할 때 디지털 서명을 추가하는 경우를 가정해서, 디지털 서명으로 변조를 확인하고 송신자를 인증하는 메커니즘은 다음과 같다.
>
> 1. 송신자가 보낼 데이터에서 해시값을 생성한다.
> 2. 생성한 해시값을 송신자(클라이언트)의 비밀키로 암호화해 서명 데이터를 작성한다.
> 3. 송신자는 데이터와 서명 데이터를 함께 수신자에게 전송한다.
> 4. 수신자(서버)는 송신자(클라이언트)의 공개키를 이용해 서명 데이터를 복호한다. 송신자의 공개키로 서명을 복호할 수 있다는 사실에서 송신자가 확실하게 대응하는 비밀키를 가지고 있음을 알 수 있다.
> 5. 수신자는 수신한 데이터로부터 해시값을 생성한다.
> 6. 수신자가 생성한 해시값과 서명의 해시값을 비교한다. 해시값이 같으면 데이터가 변조되지 않았음을 알 수 있다.



### 디지털 인증서 : 암호화에 사용할 공개키는 진짜인가?

##### 공개키는 진짜일까?

> 공개키 암호는 암호키 배송 문제를 해결한 획기적인 암호 방식이다. 키를 배송할 필요가 없고, 공개된 공개키로 암호화하면 대응하는 비밀키를 가진 수신자가 데이터를 복호할 수 있다.
>
> 공개키 암호를 안심하고 이용하기 위해서는 공개키가 진짜라는 것을 확인해야만 한다.
>
> 악의를 가진 제 3자가 수신자가되어, 공개키를 공개할 가능성이 있기 때문이다. 그렇게 되면, 그 공개키로 암호화된 모든 데이터를 악의를 가진 제 3자가 복호할 수 있게 된다.

##### 디지털 인증서

> 그런 일을 방지하기 위해, 공개키가 진짜인지 확인하고 공개키 암호를 안전하게 이용하기 위한 인프라로서 <strong>PKI</strong>(Public Key Infrastructure)가 있다.
>
> PKI에서는 <strong>인증기관</strong>(CA, Certification Authority)에서 발행한 <strong>디지털 인증서</strong>로 공개키 암호를 안전하게 이용할 수 있도록 하고 있다.
>
> CA는 신뢰할 수 있는 제 3자 기관이다. 많은 CA가 존재하고 있으며 CA끼리는 서로를 신뢰한다.
>
> 디지털 인증서 개요
>
> 1. 공개키와 비밀키를 쌍으로 생성한다. 비밀키는 엄중하게 관리해 두어야 한다.
> 2. 공개키와 소유자 정보를 CA에 보내서, 인증서 발행을 신청한다. 인증서 발행 신청을 CSR(Certificate Signaling Request)이라고 부른다.
> 3. CA는 발행 신청이 접수되면, 소유자 정보를 심사해서 문제가 없으면 인증서를 생성한다.
> 4. 생성한 인증서를 신청한 조직에 발행한다.
> 5. 발행된 인증서를 이용할 서버 등에 설치한다.



### SSL, 하이브리드 암호 : 온라인 쇼핑의 안전성을 확보한다

##### SSL

> SSL에서는 디지털 인증서로 통신 상대방이 진짜라는 것을 확인한다. 그리고 상대방에게 보내는 데이터를 암호화해서 도청을 방지한다. SSL을 이용하면, 개인정보를 안심하고 보낼 수 있다.
>
> SSL로 암호화한 웹사이트는 웹브라우저 주소창에 자물쇠 아이콘으로 표시된다. 또한, URL은 'https://'로 시작한다.

##### SSL 암호화의 흐름

> SSL 암호화는 공개키 암호 방식과 공통키 암호 방식을 조합한 <strong>하이브리드 암호</strong>이다. SSL 통신은 서버의 디지털 인증서를 가져온다. 디지털 인증서를 체크함으로써, 그 서버가 진짜 서버가 맞는지 확인한다. 디지털 인증서에는 서버의 공개키가 포함되어 있다. 공개키 암호를 사용하면 처리 부하가 크므로, 주고받는 애플리케이션 자체를 공개키로 암호화하는 것은 아니다. 인증서에 포함된 공개키는 공통키를 안전하게 배송하기 위해 사용한다. 공통키를 디지털 인증서에 포함된 공개키로 암호화해서, 클라이언트 PC와 서버가 안전하게 공유할 수 있게 한다.















