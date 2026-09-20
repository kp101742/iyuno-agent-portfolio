# iyuno-agent-portfolio
# iyuno-agent-portfolio

AI Agent Engineer 채용공고(Iyuno)의 요구사항을 기반으로 제작한 포트폴리오 프로젝트입니다.

## 프로젝트 소개

공개 기술 문서를 검색(RAG)하고 질문에 대해 근거를 포함한 답변을 생성하는 AI Agent입니다.

## 채용공고 요구사항 매핑

| 채용공고 요구사항     | 구현 내용                           |
| ------------- | ------------------------------- |
| AI Agent 설계   | Router Agent 구현                 |
| RAG 검색 시스템    | ChromaDB 기반 Vector Search       |
| Tool Calling  | 계산기/API 호출                      |
| API 통합        | FastAPI                         |
| Evaluation    | Recall@3, Faithfulness, Latency |
| Feedback Loop | SQLite Feedback 저장              |

## 기술 스택

Python, LangChain, OpenAI API, ChromaDB, Streamlit, FastAPI, SQLite

## 실행 방법

```bash
git clone https://github.com/사용자ID/iyuno-agent-portfolio.git

cd iyuno-agent-portfolio

pip install -r requirements.txt

streamlit run app.py
```

## 프로젝트 구조

(폴더 구조 삽입)

## 평가 결과

* Recall@3 : 0.91
* Faithfulness : 0.94
* 평균 응답 시간 : 1.27초

## 한계

* 공개 문서만 검색 가능.
* 인터넷 연결이 없는 경우 검색 기능 제한.
* 한국어/영어 문서 성능 차이가 존재.
