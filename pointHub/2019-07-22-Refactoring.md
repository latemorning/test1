> 2019-07-22 최초생성  
> 2019-07-23 포인트 제공처별 추가...  
> 2019-07-25 PMD 룰셋 추가 2019-07-30 리팩토리 대상  
> 2019-08-05 StdController에 다날이 추가되면서 if문 추가됨...  
> 2019-08-14 하드코딩체크

Refactoring
===========

### 공통사항

-	유효성 체크 로직이 메서드마다 중복사용
	-	공통으로 사용가능한 로직은 공통처리

패키지
------

### com.olleh.pointHub.api.sdk.controller.StdController

-	소스가 큼
-	일반결제와 페미리포인트 결제 케이스가 if문으로 구별됨
-	다날이 추가되면서 if문으로 구분함
-	결제 구분에 따라서 if문 구분
-	너무 많은 요청이 몰림

업무
----

### 포인트 제공처별

각 카드사별 사용조건이 다름

### PMD 룰셋관련 URL

-	2019-09-18 룰셋 업데이트 됨 https://www.egovframe.go.kr/wiki/doku.php?id=egovframework:dev2:imp:inspection
-	kt 자체 CodePrism 사용

### 리팩토리 대상

-	SMS/MMS 발송
	-	regMmsSendHist 메소드를 직접 호출하는 서비스를 찾아서 수정

### 하드코딩 체크

-	ClipServiceImpl.getBasicPointInfo() 탑툰 비교하는 부분

### 배치로직

-	JOB 인터페이스 생성
-	공통 메서드 구현하는 방식으로 진행
