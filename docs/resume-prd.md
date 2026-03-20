# 📄 PRD - Personal Resume Page

---

## 1. 프로젝트 개요

| 항목 | 내용 |
|------|------|
| **프로젝트명** | Personal Resume Page |
| **프로젝트 유형** | 정적 웹페이지 (단일 HTML) |
| **핵심 기능** | 자기소개서/이력서를 하나의 웹페이지로 제작 |
| **타겟 사용자** | 구직자, 프리랜서, 자기소개서 제출이 필요한 사람 |
| **예상 개발 기간** | 1일 |

---

## 2. UI/UX 요구사항

### 2.1 레이아웃 구조

```
┌─────────────────────────────────────────┐
│               HEADER                    │
│         (이름 + 간단한 타이틀)           │
├─────────────────────────────────────────┤
│              ABOUT ME                   │
│         (한 줄 자기소개)                │
├───────────────────┬─────────────────────┤
│    CONTACT        │      EDUCATION      │
│   (연락처 정보)    │     (학력 정보)      │
├───────────────────┴─────────────────────┤
│             EXPERIENCE                  │
│           (경력 사항)                    │
├─────────────────────────────────────────┤
│               SKILLS                    │
│           (보유 스킬)                   │
├─────────────────────────────────────────┤
│               FOOTER                    │
│         (카opyright 등)                 │
└─────────────────────────────────────────┘
```

### 2.2 반응형 브레이크포인트

| 디바이스 | 너비 | 레이아웃 |
|----------|------|----------|
| 모바일 | < 768px | 1단 колонка |
| 데스크탑 | ≥ 768px | 2단 그리드 (contact + education) |

### 2.3 색상 테마 (그린)

| 용도 | 색상 | Hex |
|------|------|-----|
| Primary | Forest Green | `#228B22` |
| Secondary | Light Green | `#90EE90` |
| Accent | Dark Green | `#006400` |
| Background | Off-White | `#FAFFF5` |
| Text Primary | Dark Gray | `#333333` |
| Text Secondary | Medium Gray | `#666666` |
| Border | Light Gray | `#E0E0E0` |

### 2.4 타이포그래피

| 용도 | 폰트 | 크기 |
|------|------|------|
| 이름 (Header) | Pretendard / Noto Sans KR | 32px, Bold |
| 섹션 타이틀 | Pretendard / Noto Sans KR | 20px, SemiBold |
| 본문 | Pretendard / Noto Sans KR | 16px, Regular |
| 부가정보 | Pretendard / Noto Sans KR | 14px, Regular |

### 2.5 디자인 요소

- **카드 스타일**: 배경 흰색, 그림자 `box-shadow: 0 2px 8px rgba(0,0,0,0.08)`
- **모서리**:Border Radius 8px
- **구분선**: 섹션 간 1px 실선 `#E0E0E0`
- **아이콘**: 단순化したSVG 아이콘 (연락처, 학력, 경력, 스킬)
- **애니메이션**: 없음 (정적 페이지)

---

## 3. 기능 요구사항

### 3.1 섹션별 콘텐츠

#### HEADER
- 이름 (예: 김철수)
- 직함/타이틀 (예: 프론트엔드 개발자)

#### ABOUT ME
- 한 줄 자기소개문 (예: "사용자와 가장 가깝게 만나는 개발자가 되고 싶습니다.")

#### CONTACT
- 이메일 (mailto: 링크)
- GitHub (링크)
- 블로그/포트폴리오 (링크)

#### EDUCATION
- 대학교/대학원명 + 학과 + 재학기간
- 학점 (선택)

#### EXPERIENCE
- 회사명 + 부서
- 재직기간
- 담당 업무 (핵심 2-3개)

#### SKILLS
- 보유 기술 스택 (태그 형태로 표시)

#### FOOTER
- 작성일
- 간단한 copyright 문구

### 3.2 상호작용

| 기능 | 동작 |
|------|------|
| 외부 링크 | 새 탭에서 열기 (`target="_blank"`) |
| 이메일 | 기본 메일 앱 열기 (`mailto:`) |
| 인쇄 | 인쇄 최적화 CSS 적용 |

---

## 4. 기술 스택

| 구분 | 기술 |
|------|------|
| Markup | HTML5 |
| Styling | CSS3 (inline/internal, 외부 파일 없이 단일 HTML) |
| 폰트 | Google Fonts (Noto Sans KR) |
| 아이콘 | SVG (inline) |
| 호환성 | Modern Browser (Chrome, Firefox, Safari, Edge) |

---

## 5. 파일 구조

```
resume/
└── index.html    # 단일 파일로 모든 코드 포함
```

---

## 6. 마일스톤

| Phase | 내용 | 상태 |
|-------|------|------|
| 1 | PRD 작성 | ✅ |
| 2 | HTML/CSS 구현 | ⏳ |
| 3 | 검증 (Responsive, Accessibility) | ⏳ |

---

## 7. 검증 기준

- [ ] 모바일/데스크탑 모두 정상 렌더링
- [ ] 모든 링크 정상 동작
- [ ] 폰트 정상 로드
- [ ] 색상 테마 일관성 유지
- [ ] 인쇄 시 레이아웃 유지

