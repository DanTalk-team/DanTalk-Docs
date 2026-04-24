# 📚 DanTalk-Docs

> DanTalk 프로젝트의 기획, 설계, API 명세, 회의록을 관리하는 문서 저장소입니다.

---

## 🏫 프로젝트 소개

**DanTalk**은 단국대학교 재학생만을 위한 전용 캠퍼스 커뮤니티 플랫폼입니다.
학교 이메일(Google OAuth)을 통해 재학생 인증을 하며, 학과별 게시판, 시간표 관리, 학교 주변 맛집 정보, 그리고 단국대 데이터로 학습된 AI 챗봇을 제공합니다.

---

## 👥 팀 구성

| 역할        | 담당                           |
| ----------- | ------------------------------ |
| 백엔드 개발 | Spring Boot 기반 REST API 개발 |
| 프론트엔드  | Next.js 기반 UI 개발           |
| 디자인      | Figma UI/UX 설계               |

---

## 🛠️ 기술 스택

### Frontend

![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)

### Backend

![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![Java](https://img.shields.io/badge/Java-007396?style=for-the-badge&logo=java&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)

### AI Server

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)

### AI Model

- LLaMA 3.2 3B + LoRA Fine-tuning
- 단국대 공지사항 / FAQ / 학사 데이터 학습

### Infra & Tools

![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)
![Jira](https://img.shields.io/badge/Jira-0052CC?style=for-the-badge&logo=jira&logoColor=white)
![Figma](https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white)

---

## 📋 주요 기능

### 1. 🔐 회원가입 / 로그인

- Google OAuth 로그인 (단국대 이메일 `@dankook.ac.kr` 전용)
- 학교 이메일 외 도메인 가입 차단
- 첫 로그인 시 학번 / 학과 / 학년 추가 입력 (온보딩 페이지)

### 2. 📝 게시판

- 자유 게시판
- 학과별 게시판 (학과 인증 후 접근 가능)
- 게시글 작성 / 수정 / 삭제 / 댓글
- 신고 시스템 (커뮤니티 자정 기능)

### 3. 📅 시간표 _(여유되면 추가)_

- 직접 시간표 입력 및 관리
- 학기별 시간표 저장

### 4. 🍽️ 학교 주변 맛집

- 단국대 주변 맛집 정보 제공
- 카카오맵 API 연동

### 5. 🚌 실시간 버스 정보 _(여유되면 추가)_

- 학교 주변 실시간 버스 도착 정보

### 6. 🤖 AI 챗봇 ( 가능하면 추가 )

- 단국대 데이터(공지사항, FAQ, 학사정보)로 Fine-tuning된 LLaMA 3.2 3B 모델
- 학교 생활 관련 질문 답변
- FastAPI 서버로 서빙 후 Spring과 연동

---

## 🏗️ 시스템 아키텍처

```
Next.js (Frontend)
    ↓               ↓
Spring Boot      FastAPI (AI Server)
(메인 API)            ↓
    ↓          LLaMA 3.2 3B
  MySQL DB
```

---


## 🔗 관련 저장소

| 저장소           | 설명                        |
| ---------------- | --------------------------- |
| DanTalk-Backend  | Spring Boot 백엔드          |
| DanTalk-Frontend | Next.js 프론트엔드          |
| DanTalk-AI       | FastAPI + LLaMA Fine-tuning |
| DanTalk-Docs     | 📌 현재 저장소              |
