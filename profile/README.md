<div align="center">

# 📋 miniDooray

**NHN 두레이(Dooray)를 벤치마킹한 협업 툴 클론 프로젝트**

MSA 기반으로 설계한 프로젝트·태스크·마일스톤·멤버 관리 협업 서비스

*NHN Academy AIOT 3기 · Team 11 · 2026.05.14 ~ 2026.05.22*

</div>

---

## 🧩 서비스 구성

Gateway를 단일 진입점으로 하여 계정 관리와 태스크 관리를 별도 서비스로 분리한 MSA 구조입니다.

```
Client
  │
  ▼
Gateway (8000)  ── 라우팅 · 글로벌 로깅
  ├── Account API (8081) ── 계정 관리
  └── Task API    (8082) ── 프로젝트 · 태스크 · 마일스톤 · 멤버 · 댓글
        │
        └── (내부 호출) Account API

FE (8080) ── Spring MVC + Thymeleaf, Redis 세션
```

| 서비스 | 설명 | Repository |
|---|---|---|
| 🌐 Gateway | 요청 라우팅 · 글로벌 로깅 (Spring Cloud Gateway) | [miniDooray-Gateway](https://github.com/AIOT3-miniDooray-team11/miniDooray-Gateway) |
| 👤 Account API | 계정 등록 · 조회 · 수정 · 삭제 | [miniDooray-AccountAPI](https://github.com/AIOT3-miniDooray-team11/miniDooray-AccountAPI) |
| ✅ Task API | 프로젝트 · 태스크 · 마일스톤 · 멤버 · 댓글 관리 | [miniDooray-TaskAPI](https://github.com/AIOT3-miniDooray-team11/miniDooray-TaskAPI) |
| 🖥️ FE | Thymeleaf 기반 웹 화면, 인증/세션 처리 | [miniDooray-FE](https://github.com/AIOT3-miniDooray-team11/miniDooray-FE) |

## 🛠 기술 스택

![Java](https://img.shields.io/badge/Java_21-007396?style=flat&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot_4.0.6-6DB33F?style=flat&logo=springboot&logoColor=white)
![Spring Cloud Gateway](https://img.shields.io/badge/Spring_Cloud_Gateway-6DB33F?style=flat&logo=spring&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=flat&logo=springsecurity&logoColor=white)
![Spring Data JPA](https://img.shields.io/badge/Spring_Data_JPA-6DB33F?style=flat&logo=spring&logoColor=white)
![Thymeleaf](https://img.shields.io/badge/Thymeleaf-005F0F?style=flat&logo=thymeleaf&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=mysql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=redis&logoColor=white)
![Maven](https://img.shields.io/badge/Maven-C71A36?style=flat&logo=apachemaven&logoColor=white)
![SonarQube](https://img.shields.io/badge/SonarQube-4E9BCD?style=flat&logo=sonarqube&logoColor=white)

## 👥 Team 11

| 이름 | GitHub | 담당 |
|---|---|---|
| 김동건 | [@hetgwi01](https://github.com/hetgwi01) | Account API · Task API (마일스톤 · 멤버) |
| 조창희 | [@SRIOUSS](https://github.com/SRIOUSS) | Gateway · FE |
| 손재민 | [@woalshue](https://github.com/woalshue) | Gateway · FE |
| 전재나 | [@jaena9958-art](https://github.com/jaena9958-art) | Task API |

---

<div align="center">

*NHN Academy AIOT 3기 Team 11*

</div>
