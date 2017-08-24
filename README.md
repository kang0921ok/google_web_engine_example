## Google App Engine 바로 설정하기
- 2017.8.25 기준
- 빌링 셋팅 과정이 필요합니다. 진행 하시다가 필요하다고 나오면 하면 됩니다.

### google app engine console에서 배포하는 방법
1. https://console.cloud.google.com/projectcreate 프로젝트 생성
2. https://console.cloud.google.com/appengine/start 앱엔진 접근
3. 첫번째 앱 클릭 
4. 언어는 자바 기준
5. 앱 제공 지역 선택 asia-northeast1
6. App Engine 빠른시작을 끝까지 진행하면 PROJECT_ID의 폴더가 생깁니다. (감을 익히세요)
7. Google Cloude Shell을 오픈
8. git clone 해당 프로젝트
9. gcloud config set project YOUR_PROJECT_ID
 - YOUR_PROJECT_ID는 YOUR_PROJECT_ID@appspot.com 입니다.
10. mvn appengine:deploy (오래걸립니다.)
11. YOUR_PROJECT_ID@appspot.com 가 도메인입니다.
12. 위의 과정이 flex java8 배포

구글 공식 가이드 : https://cloud.google.com/appengine/docs/flexible/java/quickstart
