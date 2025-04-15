# 📘 사이트 이름 및 개요

학생들이 문제를 직접 풀고, **즉각적인 피드백**을 받으며, **누적 학습 데이터를 기반으로 맞춤형 학습**을 할 수 있는 웹 플랫폼

---

## 📦 주요 기능

- **사용자 맞춤 문제 추천**
  - 학년, 학기, 단원 선택 (예: 중2 > 1학기 > 함수)
  - 난이도 선택 (하, 중, 상)
  - 랜덤 문제 추천 또는 맞춤 문제 추천 (이전 풀이 이력 기반)

- **문제 풀이 인터페이스**
  - 문제 이미지 또는 텍스트 + 수식 렌더링
  - 수식 입력창 제공 (`MathQuill`, `KaTeX`, `MathJax` 등 활용)
  - 제출 시 즉시 정오 판별
  - 모범답안 및 풀이 과정 출력

- **피드백 시스템**
  - 틀린 문제: 오답 원인 힌트 제공
  - 정답일 경우: 유사 고난이도 문제 추천
  - 선택형 문제: 정답률/오답률/해설 제공

- **학습 리포트**
  - 오늘 푼 문제 수, 정확도, 단원별 성취도
  - 주간/월간 학습 통계 (그래프 시각화)
  - 취약 단원 자동 추천

- **로그인 기능 (선택 사항)**
  - 학부모 / 학생 / 교사 계정 분리
  - 학생: 풀이 기록 저장
  - 교사: 문제 추천 / 과제 출제

---

## 🌟 부가 기능 아이디어

- 틀린 문제 마크 기능 (즐겨찾기)
- 친구와 문제 공유 / 풀기 챌린지
- 하루 추천 문제 알림 (Firebase 활용)

---

## 🧱 기술 구조

| 계층 | 기술 |
|------|------|
| **프론트엔드** | React (Vite + Axios + Tailwind + React Router) |
| **백엔드 (서비스 로직)** | Spring Boot (회원 관리, 리포트 처리, 문제 이력 저장) |
| **데이터 제공 API** | Python + FastAPI + Uvicorn (AI Hub 수학 문제 제공) |
| **DB** | MySQL (유저, 문제, 풀이 이력, 통계) |
| **배포** | Docker + AWS EC2 (추후 S3 + Nginx + HTTPS 고려 가능) |
