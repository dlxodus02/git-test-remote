# Hard-Click Backend

Hard-Click 백엔드 팀 공용 협업 레포지토리입니다.

## 목적

- 백엔드 서비스 코드와 관련 문서를 함께 관리합니다.
- 협업 규칙을 통일해 리뷰와 배포 흐름을 단순하게 유지합니다.
- API, 아키텍처, 운영 규칙을 문서로 남겨 팀 지식을 축적합니다.

## 시작하기

```bash
git clone <repository-url>
cd <repository-name>
```

필요한 실행 방법과 개발 환경 설정은 프로젝트 스택에 맞춰 추가해 주세요.

## 기본 구조

```text
.
├─ .github/
│  ├─ ISSUE_TEMPLATE/
│  └─ pull_request_template.md
├─ docs/
│  ├─ api-spec.md
│  ├─ architecture.md
│  ├─ convention.md
│  ├─ labels.md
│  └─ milestones.md
├─ .gitignore
└─ README.md
```

## 브랜치 전략

- `main`: 운영 반영 기준 브랜치
- `develop`: 통합 개발 브랜치
- `feature/*`: 기능 개발
- `fix/*`: 버그 수정
- `hotfix/*`: 긴급 운영 대응

예시:

```text
feature/user-signup
fix/login-token-refresh
hotfix/payment-timeout
```

## 커밋 메시지 규칙

아래 형식을 권장합니다.

```text
type: summary
```

예시:

```text
feat: 회원가입 API 추가
fix: 토큰 만료 검증 오류 수정
docs: 배포 절차 문서화
refactor: 주문 서비스 책임 분리
test: 인증 서비스 테스트 추가
```

추천 타입:

- `feat`
- `fix`
- `docs`
- `refactor`
- `test`
- `chore`

## PR 규칙

- PR은 가능한 한 작은 단위로 올립니다.
- 리뷰어가 빠르게 이해할 수 있도록 변경 배경을 적습니다.
- API 변경, DB 스키마 변경, 환경변수 추가 여부를 명시합니다.
- 머지 전 테스트 결과를 확인합니다.

## 문서

- [협업 컨벤션](docs/convention.md)
- [아키텍처 개요](docs/architecture.md)
- [API 명세 작성 가이드](docs/api-spec.md)
- [이슈 라벨 가이드](docs/labels.md)
- [마일스톤 가이드](docs/milestones.md)

## 이슈 템플릿

- `Feature`: 기능 개발용
- `Refactor`: 구조 개선용
- `Daily`: 일일 작업 공유용
- `Bug report`: 버그 제보용

## 마일스톤 운영

- `Sprint`: 기간 단위 작업 관리
- `Release`: 배포 단위 관리
- `Epic`: 도메인/기능 묶음 관리

## 다음 추천 작업

1. GitHub에서 새 레포를 생성합니다.
2. 이 폴더에서 `git init` 후 첫 커밋을 만듭니다.
3. 원격 저장소를 연결하고 `main` 브랜치에 푸시합니다.
4. 팀 스택에 맞춰 실행 방법, 디렉터리 구조, CI 설정을 추가합니다.
