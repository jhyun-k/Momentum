# Momentum
사용자 이름 입력, 투두리스트, open weather API 이용하여 날씨 정보 불러오기, 로컬스토리지에 정보 저장, 불러오기, 삭제 기능을 구현한 Momentum 웹 어플리케이션입니다.

## 기능소개
### 1. 초기화면
![chrome_rXDCRdIlz6](https://github.com/jhyun-k/Momentum/assets/105181266/7a719ef0-54cb-4c4a-ac4d-b74fe2141033)

### 2. 사용자 이름 입력
![chrome_83ennuY8fJ](https://github.com/jhyun-k/Momentum/assets/105181266/a3045234-a4b8-4406-8744-a277572ff4ef)

### 3. 투두리스트 추가, 삭제, 체크 기능
![chrome_Hyb47pVgNr](https://github.com/jhyun-k/Momentum/assets/105181266/ec57de4b-456c-44f7-8f43-dbcbc66ce531)

### 4. 새로고침하여도 정보 유지
![chrome_RBHFpHSo4l](https://github.com/jhyun-k/Momentum/assets/105181266/a46f2a51-4ebf-4607-a2c4-2f9460ef9fbc)

### 5. 로그아웃기능
![chrome_DvpfXKQXEz](https://github.com/jhyun-k/Momentum/assets/105181266/d403bd12-98ee-4f4e-9bad-4cdcde2f6771)

## 트러블슈팅
1. `setInterval` 로 시계를 만들었는데 delay를 1초인 1000으로 설정해놓으니 시계가 뜨는 것도 1초 후에 떠서 문제가 생겼다. 이를 해결하려 찾아보니 먼저 getTime이라는 시계생성함수를 즉시실행함수로 먼저실행한 후 setInterval 함수를 이용해야 화면이 켜지는 즉시 시계가 뜨고 1초마다 초가 바뀐다.

2. 투두리스트를 추가할 때 `flex` 로 정렬해놓다보니 추가할때마다 크기가 점점 늘어나서 인사와 시계를 밀어버리는 상황이 일어났다. 이를 막고자 투두리스트를 감싸는 컨테이너를 만들어 height 를 지정하니 해결되었다.

3. 투두리스트 flex 의 `justify-content` 를 `space-between`으로 해놓으니 투두리스트가 아래부터 추가되고, center로 하니 또 자꾸 크기가 늘어났다. 속성을 flex-start로 바꾸자 정상적으로 처음부터 생성되었다.

4. 로그아웃 기능을 구현할 때 사용자이름을 입력하고 새로고침을 하지 않으면 기능이 동작하지 않았다. enter키 입력 이벤트를 할 때에는 logoutBtn 변수가 할당되어있지 않아서 발생하는 문제였다. enter키 입력 이벤트 함수 안에도 logout함수를 넣으니 해결되었다.
