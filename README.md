# iyuno-agent-portfolio

## 1. 프로젝트 소개

Iyuno AI Agent Engineer 채용공고를 분석하고,
채용공고에서 요구하는 AI Agent 관련 기술을 직접 구현하여
GitHub 포트폴리오로 정리하는 프로젝트입니다.

## 2. 채용공고

**기업:** Iyuno  
**직무:** AI Agent Engineer  
**근무 형태:** 서울 · Hybrid · Full-time

### 채용공고 링크

https://iyuno.wd3.myworkdayjobs.com/careers/job/seoul/ai-agent-engineer_jr101122

## 3. 주요 요구사항

채용공고에서 확인한 주요 요구사항을 바탕으로 다음 기능을 구현할 예정입니다.

- LLM 기반 AI Agent 시스템 설계 및 개발
- RAG 검색 및 응답 시스템
- Tool Calling 및 API 연동
- 데이터베이스 통합
- 다단계 Workflow
- 평가 및 Feedback Loop
- Latency, Cost, Reliability 개선

## 4. 프로젝트 목표

공개된 보안·기술 문서를 활용하여 사용자의 질문에 답변하고,
답변의 근거가 되는 문서를 함께 제시하는 AI Agent를 구현합니다.

## 5. 구현 예정 기능

- 공개 문서 수집 및 전처리
- 문서 Chunking
- Embedding
- Vector Search
- RAG 기반 답변
- 답변 근거 Citation
- Tool Calling
- API 연동
- 성능 평가 및 오류 분석

## 6. 개발 과정

본 프로젝트는 AI를 개발 보조 도구로 활용하여 단계적으로 구현합니다.

- 프로젝트 구조 설계
- 기능별 구현
- 오류 분석 및 수정
- 테스트
- 성능 평가
- 웹 데모 구현

## 7. 현재 진행 상황

### Week 1

## 8. 프로젝트의 한계

프로젝트 진행 과정에서 구현하지 못한 기능이나
성능상의 한계를 정리하여 최종 README에 기록할 예정입니다.

# Iyuno AI Agent Ecosystem

Iyuno의 미디어 번역 및 로컬라이제이션 워크플로우 지원을 위한 **RAG + Tool Calling + Evaluation + Streamlit** 기반 AI Agent 프로토타입입니다.

---

## 🔑 Key Features

1. **Context-Aware RAG Engine (`src/rag/`)**
   - 용어집(Glossary) 및 도메인 가이드를 파싱하여 Vector DB(Chroma)에 색인합니다.
   - 쿼리 의도에 따라 상위 $K$개 관련 맥락을 추출하여 LLM 환각 현상을 최소화합니다.

2. **Function Calling / Tool Integration (`src/agent/`)**
   - 외부 API 연동(번역 검증, 용어 사전 검색, 자막 타임코드 검증 등)을 수행하는 커스텀 Tool 구현.
   - LLM이 자율적으로 어떤 도구를 호출할지 판단하여 정밀한 태스크를 실행합니다.

3. **System Evaluation (`src/eval/`)**
   - RAG 파이프라인 및 에이전트 답변 정밀도 평가 (Ragas 기반 Faithfulness, Relevancy 측정).
   - Tool Calling 선택 및 실행 정확도를 검증합니다.

4. **Interactive Streamlit Interface (`app.py`)**
   - 에이전트의 Reasoning Step(생각 과정 및 Tool 호출 로그)을 실시간 스트리밍으로 시각화합니다.

---

## 🛠 Tech Stack

- **Language:** Python 3.11+
- **LLM Orchestration:** LangChain / LangGraph
- **Vector DB:** ChromaDB
- **UI Framework:** Streamlit
- **Evaluation:** Ragas / TruLens

---

## 🚀 Quick Start

### 1. 환경 설정 및 가상환경 구축

```bash
# 레포지토리 클론
git clone [https://github.com/your-username/iyuno-ai-agent.git](https://github.com/your-username/iyuno-ai-agent.git)
cd iyuno-ai-agent

# 가상환경 생성 및 활성화
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# 의존성 패키지 설치
pip install -r requirements.txt
