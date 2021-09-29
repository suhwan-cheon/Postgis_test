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
![image](https://user-images.githubusercontent.com/52690419/135284154-1704f0a7-49b7-44cd-9382-e28c2a1e92b1.png)
그 다음 이름만 마음대로 수정하고 save를 클릭 default db가 생성된 것을 볼 수 있습니다.

### 6. postgis extension 생성
생성한 db를 클릭한 후 상단의 Tools에서 Query Tool에 접근해줍니다.
![image](https://user-images.githubusercontent.com/52690419/135284512-8e25169a-e135-49ee-b72d-81afaf395f84.png)

다음과 같이 따라 친 후 상단의 재생 버튼을 눌러주세요
<img width="1013" alt="스크린샷 2021-09-29 오후 11 05 10" src="https://user-images.githubusercontent.com/52690419/135284722-b5606db5-00fe-481e-91e7-89fbd4f4bb53.png">

그럼 오른쪽 하위메뉴 extension에 postgis가 생긴 것을 확인할 수 있습니다.


