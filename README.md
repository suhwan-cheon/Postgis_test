# Postgis_test

Postgresql, Postgis 연습용 저장소

mac 환경

### 1. postgresql 설치

```
brew install postgresql
```

### 2. postgis 설치

```
brew install postgis
```

### 3. postgresql 실행

```
brew services start postgresql
psql postgres
```

### 4. pgadmin4 설치
Postgresql을 관리하기 쉽게 GUI환경을 제공하는 툴입니다. 현재 최신버전은 Pgadmin4
공식 홈페이지 : https://www.pgadmin.org/download/

![image](https://user-images.githubusercontent.com/52690419/135281956-d79aba82-c43a-4b6a-a981-a6d0b0deef0b.png)

다운로드 후 실행 시 이런 페이지가 나오면 완료!

### 5. database 생성
pgAdmin에 처음 들어가게되면 아래와 같은 목록이 오른쪽 화면에 보입니다.
![image](https://user-images.githubusercontent.com/52690419/135283983-890e6d16-be4a-4f8a-be30-e310b26788f5.png)

여기서 database 부분을 마우스 우클릭 후 create 클릭해줍시다.
![image](https://user-images.githubusercontent.com/52690419/135285032-e561ac42-ec13-4fb4-8102-b2fd37cc1a81.png)

그 다음 이름만 마음대로 수정하고 save를 클릭 default db가 생성된 것을 볼 수 있습니다.

### 6. postgis extension 생성
생성한 db를 클릭한 후 상단의 Tools에서 Query Tool에 접근해줍니다.
![image](https://user-images.githubusercontent.com/52690419/135284512-8e25169a-e135-49ee-b72d-81afaf395f84.png)

다음과 같이 따라 친 후 상단의 재생 버튼을 눌러주세요 (또는 f5)
<img width="1013" alt="스크린샷 2021-09-29 오후 11 05 10" src="https://user-images.githubusercontent.com/52690419/135284722-b5606db5-00fe-481e-91e7-89fbd4f4bb53.png">

그럼 오른쪽 하위메뉴 extension에 postgis가 생긴 것을 확인할 수 있습니다.

또한 새로고침 시 schema - functions 에서 postgis 관련 함수들이 잔뜩 생겨난 걸 볼 수 있습니다.
![image](https://user-images.githubusercontent.com/52690419/135285374-47428ad1-5518-4e03-a099-cc16dff59cc9.png)


### 7. 한국식 좌표 변환
PostGIS에서 지원하는 한국 좌표계는 변환하는 데 필요한 인자들이 잘못되어 있어 수정이 필요하다고 합니다.
아래의 링크에서 SQL 파일을 다운받아 실행해줍니다.
https://www.osgeo.kr/205

이후 database - [Query Tools] 로 들어가 다운받은 파일을 오픈해준 후 재생 버튼을 눌러주세요.
<img width="1025" alt="스크린샷 2021-09-30 오전 10 03 33" src="https://user-images.githubusercontent.com/52690419/135368897-bdd65b31-d496-49f5-8e8c-38f9729ef6b0.png">

### 8. QGIS 설치

QGIS는 데이터 뷰, 편집, 분석을 제공하는 크로스 플랫폼 자유-오픈 소스 데스크톱 지리 정보 체계 응용 프로그램입니다.
QGIS는 PostgreSQL에 있는 공간정보를 불러와 바로 시각화할 수 있기 때문에 사용한다고합니다.
저는 "안정적인 버전" 이라고 쓰여있는 3.16 버전을 다운받았습니다. (용량이 많이 크네요 😭)
다운로드 링크 : https://qgis.org/ko/site/

❗️ 주의 : mac은 보안 인증을 못 받아서 강제로 열어야합니다. 저는 마우스 우클릭 후 option을 누른채 열기를 눌러 열었습니다.

### 9. QGIS에서 맵 열기

저는 아래 깃허브에 있는 파이썬 파일을 이용했습니다.
https://github.com/giswqs/qgis-earthengine-examples/blob/master/Basemaps/qgis_basemaps.py

해당 파일을 데스크탑에 다운받은 후, qgis에서 파일을 열고, 실행(run)해줍시다. 대략적인 방법은 아래와 같습니다.
<img width="1149" alt="스크린샷 2021-09-30 오전 10 37 48" src="https://user-images.githubusercontent.com/52690419/135371471-4fa6017b-14d7-4857-9c15-49cab33085a6.png">

이후 왼쪽 창에서 XYZ 타일 하위 목록에 보면 여러가지 지도가 생긴 것을 확인할 수 있습니다.
저는 구글 하이브리드 위성 지도를 통해 우리학교를 찾아보았습니다.
![image](https://user-images.githubusercontent.com/52690419/135371745-43120948-9f7f-4da4-ade3-87b1b3df93f6.png)


