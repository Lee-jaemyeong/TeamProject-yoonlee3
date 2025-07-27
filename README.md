# yoonlee3
![스크린샷_27-7-2025_13048_](https://github.com/user-attachments/assets/05e00f73-9ee7-46c6-b830-4c80146b1eb3)

## 배포 사이트
- http://3.39.192.82:8080/

## Team GitHub
- https://github.com/Lee-jaemyeong/team-repository

### 목차
- 1️⃣ [프로젝트 개요](#프로젝트-개요)
- 2️⃣ [기술 스택](#기술-스택)
- 3️⃣ [담당 기능](#담당-기능)
- 4️⃣ [데이터 베이스 설계](#데이터-베이스-설계)
- 5️⃣ [트러블 슈팅](#트러블-슈팅)
- 6️⃣ [느낀 점](#느낀-점)

### 프로젝트 개요
목표 달성을 위한 동기 부여와 소통을 돕기 위해 만든 웹 기반 **일기 공유 플랫폼**입니다.
개인은 자신의 일기를 작성하고 관리할 수 있으며, 선택적으로 다른 사용자와 일기를 공유하거나 그룹을 만들어 함께 목표를 세우고 달성률을 나눌 수 있습니다.

### 기술 스택
⚙️ Back-End
- Spring Boot 2.7.14
- Spring Security 5.0.7
- JPA (Hibernate) 2.7.14
- Lombok 1.18.28
- Spring DevTools 2.7.14

🌐 Front-End
- Thymeleaf 3.0.15
- HTML5 / CSS3 / JavaScript
- jQuery 3.7.1

🗄 Database & Server
- MySQL 8.0.33
- Apache Tomcat 9.0.78

💻 협업 & 배포
- GitHub – 소스코드 버전 관리

### 담당 기능
#### 📺 시연 영상

[![Watch the video](https://img.youtube.com/vi/F6DzPczeOM4&t=4s/hqdefault.jpg)](https://www.youtube.com/watch?v=F6DzPczeOM4&t=4s)

1. 유저,글 CRUD 설계 및 기능 구현
2. Spring Security를 활용한 로그인 인증 및 기능구현
3. Kakao login api를 활용한 로그인,로그아웃 기능구현
4. Naver mail api를 활용한 비밀번호 찾기 및 변경 기능구현
5. 글 공개범위 필터링 구현

### 데이터 베이스 설계

### 트러블 슈팅
<details>
  <summary><strong>1. 카카오 로그아웃 실패</strong></summary>
  • <strong>문제 상황</strong>: 카카오 로그아웃 시, 세션 쿠키가 정상적으로 삭제되지 않아 사용자가 로그아웃해도 자동으로 로그인 상태가 유지되는 현상이 발생 <br/>→ 보안 취약점 존재
  <br/>
  <br/>
  • 원인 분석: 카카오 로그아웃 API 호출 또는 로그아웃 URL 리다이렉션이 누락 → 카카오 측 세션 및 인증 토큰이 미해제
  <br/>
  <br/>
  • 해결 방법: Spring Security 설정에 카카오 로그아웃 URL을 명시하여 로그아웃 요청 시 해당URL로 리다이렉트되도록 구현<br/> → 카카오 세션을 종료시키고, 클라이언트 쿠키도 정상적으로 삭제되도록 처리

</details>

### 느낀 점
