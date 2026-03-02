# 🏛️ YonSai IT Academy Renewal Project
> **Scalable Full-Stack Education Management System (EMS)**
> 실무 환경을 고려한 교육 관리 시스템 리뉴얼 프로젝트입니다. 단순한 UI 구현을 넘어, 데이터 무결성과 관리자 편의성을 극대화한 아키텍처를 지향합니다.

<p align="left">
  <img src="https://img.shields.io/badge/Next.js%2014-000000?style=for-the-badge&logo=nextdotjs&logoColor=white"/>
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white"/>
  <img src="https://img.shields.io/badge/Prisma%20ORM-2D3748?style=for-the-badge&logo=prisma&logoColor=white"/>
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white"/>
  <img src="https://img.shields.io/badge/CSS_Modules-000000?style=for-the-badge&logo=css3&logoColor=white"/>
</p>

---

## 🚀 Key Features

### 1. Advanced Admin Dashboard
- **Role-based Access Control (RBAC):** Next.js Middleware를 활용한 서버 사이드 권한 검증 (Admin/Teacher/Student).
- **Course Management:** 강의 카테고리(IT/SW 등)와 과정 유형(KDT/국비지원/일반)을 분리한 데이터 정규화 및 CRUD 구현.
- **Enrollment Flow:** 학생의 수강 신청부터 관리자의 승인/반려 프로세스까지 이어지는 비즈니스 로직 완비.

### 2. User Experience & Security
- **Secure Authentication:** NextAuth.js 기반의 세션 관리 및 Bcrypt 암호화 적용.
- **Real-time UI Sync:** 학생 마이페이지에서 수강 신청 상태(대기/수강중) 실시간 업데이트.
- **Responsive Design:** CSS Modules를 활용한 디자인 일관성 유지 및 성능 최적화.

---

## 🏗️ Technical Architecture

[Image of a modern web application architecture diagram showing Next.js frontend, Prisma ORM, and MySQL database connection]

- **Frontend:** Next.js 14 (App Router) - Server/Client Component 최적화 활용.
- **Database:** Prisma ORM을 통한 Type-safe한 쿼리 작성 및 MySQL 관계형 데이터 모델링.
- **Infrastructure (Planned):** AWS S3 (이미지 스토리지), AWS RDS (MySQL), Redis (캐싱).

---

## 💡 Engineering Focus
- **Data Integrity:** `Course`와 `CourseDetail` 테이블 분리를 통해 강의 정보의 확장성 확보.
- **Security First:** Middleware 기반의 전역 라우트 보호 및 JWT 기반 인증 보안 강화.
- **Scalability:** 가상 필드(courseTypeName) 유틸리티를 통한 전역 데이터 명칭 일관성 관리.

---

## 🛠️ How to Run

```bash
# 1. 의존성 설치
npm install

# 2. DB 마이그레이션 및 시딩
npx prisma db push
npx prisma db seed

# 3. 개발 서버 실행
npm run dev
