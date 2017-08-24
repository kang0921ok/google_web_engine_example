## 프로젝트설명
- 구글 앱엔진을 쉽게 사용하기 위한 스프링부트로 된 프로젝트입니다.
- 구글 앱엔진을 처음 사용하시는 분들은 아래 설정을 하시고 해당 프로젝트를 기반으로 확장하시면 쉽게 서버를 구축 할 수 있습니다.

## Google App Engine 바로 설정하기
- 2017.8.25 기준
- 빌링 셋팅 과정이 필요합니다. 진행 하시다가 필요하다고 나오면 하면 됩니다.
- YOUR_PROJECT_ID는 변수 값으로써 구글 앱엔진 프로젝트에 할당 된 ID값입니다.
- 프로젝트, 앱엔진 생성 후 https://console.cloud.google.com/appengine?project=airmoney-17**** 이런식으로 URL에 PROJECT_ID가 노출됩니다. 
- airmoney-17**** 이게 제 PROJECT_ID 입니다.

## google app engine console에서 배포하는 방법 (flexible java8 배포)
1. https://console.cloud.google.com/projectcreate 프로젝트 생성
2. https://console.cloud.google.com/appengine/start 앱엔진 접근
3. 첫번째 앱 클릭 
4. 언어는 자바 기준
5. 앱 제공 지역 선택 asia-northeast1
6. App Engine 빠른시작을 끝까지 진행하면 PROJECT_ID로 된 디렉토리가 생깁니다. (감을 익히세요)
7. 이제, 해당 프로젝트를 구글 앱엔진에 배포해보겠습니다.
8. Google Cloude Shell을 오픈 ([$] 뒤 부터는 shell에서 치면 되는 명령어 입니다.)
9. [$] cd PROJECT_ID (빠른시작을 안하신 분들은 PROJECT_ID로 된 디렉토리를 만듭니다)
10. [$] git clone https://github.com/kang0921ok/google_web_engine_example.git
11. [$] cd google_web_engine_example (clone 받은 디렉토리로 진입)
12. [$] gcloud config set project PROJECT_ID (까먹지 말고 입력해주세요)
13. [$] mvn appengine:deploy (오래걸립니다.)
14. PROJECT_ID@appspot.com가 도메인입니다.
15. PROJECT_ID@appspot.com/test 다음 URL로 테스트가 가능합니다.

구글 공식 가이드 : https://cloud.google.com/appengine/docs/flexible/java/quickstart

p.s PR환영. deploy를 빠르게 하는 방법 고민중..
