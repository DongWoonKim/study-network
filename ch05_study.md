# ch_05 이더넷과 무선 LAN

### 같은 네트워크 내에서의 전송을 반복한다

##### 서버는 멀리 떨어져 있지만...

> 주위에 있는 PC나 스마트폰 등은 서버의 애플리케이션과 서로 데이터를 주고 받는다.
>
> 서버는 대개 PC나 스마트폰과는 멀리 떨어진 다른 네트워크에 접속되어 있다. 기술적인 관점에서 '네트워크'는 라우터 또는 레이어3 스위치로 구획되는 범위이다. 네트워크의 기본적인 구성은 레이어2 스위치 하나의 네트워크를 구성하고, 라우터 또는 레이어3 스위치로 각 네트워크를 서로 연결하는 것이다.

##### 같은 네트워크 내의 전송을 반복해 간다

> 다른 네트워크에 접속된 서버까지의 데이터 전송은 같은 네트워크 내의 전송을 반복해감으로써 실현한다.

##### 자주 이용하는 것은 이더넷과 무선 LAN(Wi-Fi)

> 같은 네트워크 내에서 전송하는 프로토콜을 이용하는 것이 이더넷과 무선 LAN(Wi-Fi)이다. TCP/IP 계층 구종에서 맨 아래인 네트워크 인터페이스층에 있는 프로토콜이다.



### 데이터를 전송하는 이더넷

##### 데이터를 전송하는 것이 이더넷

> 이더넷은 TCP/IP 계층에서 맨 아래인 네트워크 인터페이스층의 프로토콜이다. 
>
> 이더넷은 같은 네트워크 내의 어떤 이더넷 인터페이스부터 다른 이더넷 인터페이스까지 데이터를 전송한다. 같은 레이어2 스위치에 연결된 PC는 같은 네트워크에 접속된 것이다.

##### 유선 네트워크를 만든다

> 이더넷 인터페이스가 있는 기기끼리 연결해서, 이더넷 링크를 만들면 유선 네트워크가 된다.



### 이더넷의 규격

##### 이더넷에는 다양한 규격이 있다

> 이더넷에는 10Mbps에서부터 1000Gbps라는 매우 빠른 속도를 지원하는 다양한 규격이 있다. 규격은 <strong>IEEE802 위원회</strong>에서 결정된다. 이더넷의 다양한 규격은 주로 최대 전송 속도와 이용하는 매체(케이블)에 따라 나뉜다.

<table border>
  <thead>
    <tr>
      <th colspan=2>규격 이름</th>
      <th></th>
      <th>전송 속도</th>
      <th>전송 매체</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td colspan=2>IEEE802.3</td>
      <td >10BASE5</td>
      <td rowspan=3>10Mbps</td>
      <td >동축 케이블</td>
    </tr>
    <tr>
      <td colspan=2>IEEE802.3a</td>
      <td >10BASE2</td>
      <td>동축 케이블</td>
    </tr>
    <tr>
      <td colspan=2>IEEE802.3i</td>
      <td >10BASE-T</td>
      <td>UTP 케이블(카테고리3 이상)</td>
    </tr>    
    <tr>
      <td rowspan=2 colspan=2>IEEE802.3u</td>
      <td>1000BASE-TX</td>
      <td rowspan=2>100Mbps</td>
      <td>UTP 케이블(카테고리3 이상)</td>
    </tr>
    <tr>
      <td>1000BASE-FX</td>
      <td>광섬유 케이블</td>
    </tr>    
    <tr>
      <td rowspan=2 colspan=2>IEEE802.3z</td>
      <td>1000BASE-SX</td>
      <td rowspan=3>1000Mbps</td>
      <td>광섬유 케이블</td>
    </tr>
    <tr>
      <td>1000BASE-LX</td>
      <td>광섬유 케이블</td>
    </tr>
    <tr>
      <td colspan=2>IEEE802.3ab</td>
      <td>1000BASE-T</td>
      <td>UTP 케이블(카테고리5e 이상)</td>
    </tr>    
    <tr>
      <td colspan=2>IEEE802.3ae</td>
      <td>10GBASE-LX4</td>
      <td rowspan=2>10Gbps</td>
      <td>광섬유 케이블</td>
    </tr>
    <tr>
      <td colspan=2>IEEE802.3an</td>
      <td>10BASE-T</td>
      <td>UTP 케이블(카테고리6A 이상)</td>
    </tr>     
  </tbody>
</table>

##### 이더넷 규격의 명칭

> 이더넷의 규격의 명칭에는 IEEE802.3으로 시작되는 이름과 1000BASE-T처럼 전송 속도(전송 속도란 물리적인 신호로 데이터를 변환하여 전달하는 최대 속도이다.)와 전송 매체의 특징을 조합한 이름이 있다.
>
> 중요한 것은 전송 속도와 전송 매체이다.
>
> `1000 BASE - T` 
>
> 우선, 맨 앞의 숫자는 전송 속도를 나타낸다. 기본적으로 단위는 Mbps 단위이다. 
>
> 'BASE'는 베이스 밴드 방식이라는 의미이다. 현재는 베이스 밴드 방식 이외는 사용하지 않는다.
>
> '-' 뒤는 전송 매체나 물리 신호 변환의 특징을 나타낸다. 'T'가 있는 경우는 전송 매체로 UTP 케이블을 이용한다. UTP케이블은 흔히 말하는 LAN 케이블로 가장 자주 이용되는 전송 매체이다.
>
> 덧붙여, 초기 이더넷 규격은 BASE 뒤에 숫자가 기재된다. 숫자가 오는 경우는 전송 매체로 동축 케이블을 이용하고, 100m 단위 케이블의 최대 길이를 의미한다.



### 인터페이스는 어느 것?

##### 인터페이스를 특정한다

> 이더넷은 이더넷 인터페이스 간에 데이터를 전송하므로, 데이터를 전송하려면 이더넷 인터페이스를 특정해야만 한다. 이더넷 인터페이스를 특정하기 위해서는 <strong>MAC주소</strong>가 있다.

##### MAC 주소란?

> MAC 주소란 이더넷 인터페이스를 특정하기 위한 48비트 주소이다. MAC주소의 48비트 중 선두 24비트는 OUI, 그 뒤 24비트는 시리얼 넘버로 구성된다.
>
> OUI 이더넷 인터페이스를 제조하는 벤더(메이커) 식별 코드이다.
>
> 시리얼 넘버는 각 벤더가 할당한다.
>
> MAC주소는 이더넷 인터페이스에 미리 할당되어 있어, 기본적으로 변경할 수 없는 주소이므로 '물리 주소'나 '하드웨어 주소'라고 부르는 경우도 있다.

##### MAC 주소의 표기

> MAC 주소는 16진수로 표기한다.
>
> - 1바이트씩 16진수로 변환하고 '-'로 구분한다.
>
>   00-00-01-02-03-04
>
> - 1바이트씩 16진수로 변환하고 ':'로 구분한다.
>
>   00:00:01:02:03:04
>
> - 2바이트씩 16진수로 변환하고 '.'으로 구분한다.
>
>   0000.0102.0304



### 일반적으로 사용되는 인터페이스와 케이블은?

##### 자주 사용하는 이더넷 규격

> 이더넷에는 다앙한 규격이 있고, 규격마다 사용할 수 있는 인터페이스와 케이블이 다르다. 
>
> 다양한 이더넷 규격 중에서 가장 널리 이용되는 규격으로는 '10BASE-T', '100BASE-T', '1000BASE-T', '10GBASE-T'를 들 수 있다. 
>
> 이 규겨들 모두 <strong>RJ-45 이더넷 인터페이스</strong>와 <strong>UTP케이블</strong>을 채용하고 있다.

<table border>
  <thead>
    <tr>
      <th>카테고리</th>
      <th>최대 주파수</th>
      <th>주요 용도</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td >카테고리1</td>
      <td style="text-align:center;"> - </td>
      <td >음성 통신</td>
    </tr>  
    <tr>
      <td >카테고리2</td>
      <td style="text-align:center;"> 1MHz </td>
      <td >저속 데이터 통신</td>
    </tr>  
    <tr>
      <td >카테고리3</td>
      <td style="text-align:center;"> 16MHz </td>
      <td >
        <p><span style="display:inline-block; text-align:left;">10BASE-T</span> <span style="display:inline-block; text-align:right;">토큰링</span></p>
        <p>100BASE-T2/T4</p>
      </td>
    </tr>  
    <tr>
      <td >카테고리4</td>
      <td style="text-align:center;"> 20MHz </td>
      <td >
        <p><span style="display:inline-block; text-align:left;">카테고리3까지의 용도</span> <span style="display:inline-block; text-align:right;">ATM(25Mbps)</span></p>
        <p>토큰링(16Mbps)</p>
      </td>
    </tr>  
    <tr>
      <td >카테고리5</td>
      <td style="text-align:center;"> 100MHz </td>
      <td>
        <p><span style="display:inline-block; text-align:left;">카테고리4까지의 용도</span> <span style="display:inline-block; text-align:right;">ATM(156Mbps)</span></p>
        <p><span style="display:inline-block; text-align:left;">100BASE-TX</span> <span style="display:inline-block; text-align:right;">CDDI</span></p>        
      </td>
    </tr>  
    <tr>
      <td >카테고리5e</td>
      <td style="text-align:center;"> 100MHz </td>
      <td >
        <p>카테고리5까지의 용도</p>
        <p>1000BASE-T</p>
      </td>
    </tr>  
    <tr>
      <td >카테고리6</td>
      <td style="text-align:center;"> 250MHz </td>
      <td >
        <p><span style="display:inline-block; text-align:left;">카테고리5e까지의 용도</span> <span style="display:inline-block; text-align:right;">ATM(1.2Gps)</span></p>
        <p>ATM(622Mbps)</p>
      </td>
    </tr>  
    <tr>
      <td >카테고리6A</td>
      <td style="text-align:center;"> 500MHz </td>
      <td >10BASE-T</td>
    </tr>  
  </tbody>
</table>

##### UTP 케이블

> 흔히 말하는 LAN 케이블이 UTP 케이블이다.

##### RJ-45 이더넷 인터페이스

> RJ-45는 UTP 케이블용 인터페이스로서 UTP 케이블에 맞춰 8개의 단자가 있고, 전기신호(전류)가 흐르는 회로를 최대 4쌍 형성할 수 있다.















