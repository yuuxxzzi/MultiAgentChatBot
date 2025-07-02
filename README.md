# 🧠 MultiAgent ChatBot - MZ세대를 위한 AI 상담 시스템

[![GitHub License](https://img.shields.io/github/license/yuuxxzzi/MultiAgentChatBot)](https://github.com/yuuxxzzi/MultiAgentChatBot/blob/master/LICENSE)
[![GitHub Issues](https://img.shields.io/github/issues/yuuxxzzi/MultiAgentChatBot)](https://github.com/yuuxxzzi/MultiAgentChatBot/issues)
[![GitHub Stars](https://img.shields.io/github/stars/yuuxxzzi/MultiAgentChatBot)](https://github.com/yuuxxzzi/MultiAgentChatBot/stargazers)

> 🌟 **MZ세대의 정신 건강을 위한 멀티 에이전트 기반 AI 상담 시스템**

## 📖 프로젝트 소개

**MultiAgent ChatBot**은 MZ세대(밀레니얼 + Z세대)의 특성과 니즈에 맞춰 설계된 혁신적인 AI 상담 시스템입니다. 다양한 전문 에이전트들이 협력하여 감정 분석, 개인화된 상담, 역할극 치료, 마음챙김 등 종합적인 정신 건강 지원을 제공합니다.

### 🎯 핵심 목표
- **접근성**: 언제 어디서나 이용 가능한 24/7 AI 상담 서비스
- **개인화**: MZ세대의 특성을 반영한 맞춤형 상담 및 치료
- **전문성**: 다중 에이전트 시스템을 통한 전문적이고 체계적인 접근
- **지속성**: 지속적인 모니터링과 개선을 통한 장기적 정신 건강 관리

## ✨ 주요 기능

### 🤖 멀티 에이전트 시스템
- **🧠 감정 분석 에이전트**: 텍스트, 음성, 이미지를 통한 실시간 감정 상태 분석
- **💬 상담 에이전트**: 개인화된 상담 및 조언 제공
- **🎭 역할극 에이전트**: 상황별 역할극을 통한 치료적 접근
- **🧘 마음챙김 에이전트**: 명상, 호흡법 등 마음챙김 기법 가이드
- **📊 리포트 생성 에이전트**: 상담 기록 및 진행 상황 분석 리포트

### 🔧 핵심 기술
- **LangGraph**: 에이전트 간 복잡한 워크플로우 관리
- **다중 모달 입력**: 텍스트, 음성, 이미지 통합 분석
- **실시간 감정 인식**: 최신 AI 모델을 활용한 정확한 감정 분석
- **개인화 알고리즘**: 사용자별 맞춤형 상담 경험 제공

## 🛠 기술 스택

### Backend
- **FastAPI**: 고성능 비동기 웹 프레임워크
- **LangGraph**: 멀티 에이전트 워크플로우 엔진
- **PostgreSQL**: 사용자 데이터 및 상담 기록 저장
- **Redis**: 세션 관리 및 캐싱

### Frontend
- **React**: 모던 웹 인터페이스
- **TypeScript**: 타입 안전성 보장
- **Tailwind CSS**: 반응형 UI 디자인
- **Material-UI**: 일관된 UX/UI 컴포넌트

### AI & ML
- **OpenAI GPT**: 자연어 처리 및 대화 생성
- **Anthropic Claude**: 안전하고 신뢰할 수 있는 AI 응답
- **Perplexity**: 실시간 정보 검색 및 연구
- **Hugging Face**: 감정 분석 및 특화 모델

### DevOps & Infrastructure
- **Docker**: 컨테이너화된 배포
- **GitHub Actions**: CI/CD 파이프라인
- **HTTPS**: 보안 통신
- **GPU Support**: AI 모델 가속화

## 🚀 시작하기

### 사전 요구사항
- **Node.js** (v18 이상)
- **Python** (v3.9 이상)
- **Docker** & **Docker Compose**
- **PostgreSQL** (v13 이상)

### 1. 저장소 클론
```bash
git clone https://github.com/yuuxxzzi/MultiAgentChatBot.git
cd MultiAgentChatBot
```

### 2. 환경 변수 설정
`.env` 파일을 생성하고 API 키를 설정하세요:

```bash
cp .env.example .env
```

`.env` 파일을 편집하여 다음 항목들을 설정하세요:
```env
# AI API Keys
OPENAI_API_KEY=your_openai_api_key_here
ANTHROPIC_API_KEY=your_anthropic_api_key_here
PERPLEXITY_API_KEY=your_perplexity_api_key_here

# Database
DATABASE_URL=postgresql://username:password@localhost:5432/multiagent_chatbot

# Redis
REDIS_URL=redis://localhost:6379

# Security
SECRET_KEY=your_secret_key_here
JWT_SECRET=your_jwt_secret_here
```

### 3. 의존성 설치
```bash
# Backend 의존성
pip install -r requirements.txt

# Frontend 의존성
cd frontend
npm install
cd ..
```

### 4. 데이터베이스 설정
```bash
# PostgreSQL 데이터베이스 생성
createdb multiagent_chatbot

# 마이그레이션 실행
python manage.py migrate
```

### 5. 개발 서버 실행
```bash
# Backend 서버 (포트 8000)
python manage.py runserver

# Frontend 서버 (포트 3000)
cd frontend
npm start
```

### 6. Docker로 실행 (선택사항)
```bash
docker-compose up -d
```

## 📁 프로젝트 구조

```
MultiAgentChatBot/
├── .taskmaster/              # Taskmaster 프로젝트 관리
│   ├── tasks/               # 태스크 정의 및 추적
│   ├── docs/                # PRD 및 문서
│   └── reports/             # 복잡도 분석 리포트
├── backend/                 # FastAPI 백엔드
│   ├── agents/              # AI 에이전트 모듈
│   ├── models/              # 데이터베이스 모델
│   ├── routers/             # API 라우터
│   └── services/            # 비즈니스 로직
├── frontend/                # React 프론트엔드
│   ├── src/
│   │   ├── components/      # UI 컴포넌트
│   │   ├── pages/           # 페이지 컴포넌트
│   │   └── services/        # API 서비스
├── docs/                    # 프로젝트 문서
├── tests/                   # 테스트 파일
└── docker/                  # Docker 설정
```

## 🔧 개발 워크플로우

이 프로젝트는 **Taskmaster**를 사용하여 체계적으로 관리됩니다:

### 태스크 확인
```bash
npx task-master-ai list      # 모든 태스크 확인
npx task-master-ai next      # 다음 작업할 태스크 확인
npx task-master-ai show <id> # 특정 태스크 상세 정보
```

### 개발 진행
```bash
npx task-master-ai set-status --id=<id> --status=in-progress
# 코딩 작업 수행
npx task-master-ai update-subtask --id=<id> --prompt="진행 상황..."
npx task-master-ai set-status --id=<id> --status=done
```

## 🤝 기여하기

1. **Fork** 저장소를 생성하세요
2. **Feature Branch** 를 만드세요 (`git checkout -b feature/amazing-feature`)
3. **변경사항을 커밋**하세요 (`git commit -m 'Add amazing feature'`)
4. **Branch에 Push**하세요 (`git push origin feature/amazing-feature`)
5. **Pull Request**를 생성하세요

### 개발 가이드라인
- 코드 스타일: **PEP 8** (Python), **ESLint** (JavaScript)
- 테스트: 새로운 기능에는 반드시 테스트 코드 포함
- 문서화: 중요한 변경사항은 문서 업데이트 필수

## 📊 개발 현황

### 진행 상태
- ✅ **프로젝트 초기 설정** (완료)
- 🔄 **감정 분석 에이전트** (진행중)
- 📋 **상담 에이전트** (계획됨)
- 📋 **역할극 에이전트** (계획됨)
- 📋 **마음챙김 에이전트** (계획됨)
- 📋 **프론트엔드 UI** (계획됨)

전체 진행 상황은 [Taskmaster 태스크](/.taskmaster/tasks/)에서 확인할 수 있습니다.

## 🔒 보안 및 개인정보

- **데이터 암호화**: 모든 사용자 데이터는 암호화되어 저장
- **HTTPS 통신**: 전체 통신 구간 암호화
- **개인정보 보호**: GDPR 및 개인정보보호법 준수
- **익명화 처리**: 분석 목적의 데이터는 익명화 처리

## 📝 라이선스

이 프로젝트는 **MIT License** 하에 배포됩니다. 자세한 내용은 [LICENSE](LICENSE) 파일을 참조하세요.

## 📞 지원 및 문의

- **GitHub Issues**: [이슈 등록](https://github.com/yuuxxzzi/MultiAgentChatBot/issues)
- **이메일**: [프로젝트 이메일 주소]
- **문서**: [프로젝트 위키](https://github.com/yuuxxzzi/MultiAgentChatBot/wiki)

## 🙏 감사의 말

이 프로젝트는 MZ세대의 정신 건강 향상이라는 사회적 가치를 실현하기 위해 시작되었습니다. 모든 기여자분들께 깊은 감사를 드립니다.

---

⭐ **이 프로젝트가 도움이 되셨다면 스타를 눌러주세요!** ⭐ 