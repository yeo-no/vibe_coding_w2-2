# Vibe Coding W2-1 Project

이 프로젝트는 FastAPI와 Streamlit을 사용한 AI Agent 기반 채팅 시스템입니다.

## 🚀 프로젝트 구조

```
vibe_coding_w2-1/
├── backend/                 # FastAPI 백엔드
│   ├── app/                # 애플리케이션 코드
│   ├── tests/              # 테스트 코드
│   └── requirements.txt    # Python 의존성
│
├── frontend/               # Streamlit 프론트엔드
│   ├── app.py             # 메인 애플리케이션
│   └── requirements.txt   # Python 의존성
│
├── docs/                   # 프로젝트 문서
├── .github/               # GitHub 설정
│   ├── workflows/         # GitHub Actions
│   └── ISSUE_TEMPLATE/    # 이슈 템플릿
└── .cursor/               # Cursor IDE 설정
    └── rules/             # 개발 규칙
```

## 🤖 GitHub 자동화 기능

이 프로젝트는 다음과 같은 GitHub 자동화 기능을 제공합니다:

### 📋 Pull Request 자동화
- **자동 댓글**: PR 생성 시 환영 메시지와 체크리스트 자동 추가
- **자동 할당**: 변경된 파일에 따라 적절한 리뷰어 자동 할당
- **자동 라벨링**: PR 제목과 변경 파일에 따른 라벨 자동 추가
- **자동 코드 리뷰**: 코드 품질 분석 및 보안 검사 자동 실행
- **PR 크기 체크**: 변경 라인 수에 따른 크기 라벨 자동 추가

### 🐛 Issue 자동화  
- **환영 댓글**: 이슈 생성 시 타입별 맞춤 안내 메시지 자동 추가
- **자동 라벨링**: 이슈 제목과 내용에 따른 라벨 자동 분류
- **자동 할당**: 라벨에 따른 담당자 자동 배정
- **응답 시간 추적**: 우선순위별 목표 응답 시간 설정
- **오래된 이슈 관리**: 30일 이상 비활성 이슈 자동 관리

### 🧪 CI/CD 자동화
- **자동 테스트**: Push 및 PR 시 자동 테스트 실행
- **코드 품질 검사**: Flake8, Bandit 등을 통한 코드 품질 및 보안 검사
- **테스트 커버리지**: 코드 커버리지 측정 및 리포트 생성
- **통합 테스트**: PR 시 백엔드-프론트엔드 통합 테스트 실행

## 🏷️ 사용 가능한 라벨

### 타입별
- `bug`: 버그 및 오류
- `enhancement`: 새로운 기능 또는 개선사항  
- `documentation`: 문서 관련
- `question`: 질문 또는 도움 요청
- `test`: 테스트 관련
- `refactor`: 코드 리팩토링

### 우선순위별
- `priority-high`: 높은 우선순위
- `priority-medium`: 중간 우선순위
- `priority-low`: 낮은 우선순위

### 컴포넌트별
- `backend`: Backend 관련
- `frontend`: Frontend 관련  
- `agent`: AI Agent 관련

### 상태별
- `good first issue`: 초보자에게 적합한 이슈
- `help wanted`: 도움이 필요한 이슈
- `urgent`: 긴급 처리 필요

## 📝 기여 가이드

### Pull Request 생성 시
1. **브랜치 명명 규칙**: `feature/기능명` 또는 `fix/버그명`
2. **PR 제목 형식**: `[타입] 간단한 설명`
   - 예: `[FEAT] 채팅 API 엔드포인트 추가`
   - 예: `[FIX] Agent 응답 처리 버그 수정`
3. **PR 템플릿 작성**: 제공된 템플릿을 모두 작성해주세요

### Issue 생성 시
1. **이슈 제목 형식**: `[타입] 간단한 설명`
   - 예: `[BUG] 채팅 메시지 저장 실패`
   - 예: `[FEATURE] 새로운 검색 기능 추가`
2. **이슈 템플릿 사용**: 버그 리포트 또는 기능 요청 템플릿 사용

## 🛠️ 개발 환경 설정

### 백엔드 설정
```bash
cd backend
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
```

### 프론트엔드 설정
```bash
cd frontend  
pip install -r requirements.txt
streamlit run app.py
```

### 테스트 실행
```bash
# 백엔드 테스트
cd backend
python -m pytest tests/ -v

# 프론트엔드 테스트  
cd frontend
python -m pytest . -v
```

## 🔧 GitHub Actions 설정

### 필요한 Secrets
다음 Secrets를 GitHub 저장소에 설정해주세요:
- `LANGSMITH_API_KEY`: LangSmith API 키 (Agent 모니터링용)

### 워크플로우 실행
- **CI 테스트**: Push 및 PR 시 자동 실행
- **라벨 설정**: 수동 실행 (`Actions` → `GitHub 라벨 설정` → `Run workflow`)

## 📞 문의 및 지원

프로젝트 관련 문의사항이나 버그 신고는 GitHub Issues를 통해 문의해주세요.

- 🐛 [버그 리포트](../../issues/new?template=bug_report.md)
- ✨ [기능 요청](../../issues/new?template=feature_request.md)

---

**자동화된 GitHub 관리 시스템**으로 효율적인 협업을 경험해보세요! 🚀 