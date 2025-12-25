---
title: "[PT] Development of an Intelligent Organizational Knowledge Management System using Hybrid Search and Agent Workflows"
collection: publications
category: conferences
permalink: /publication/2025-11-07-paper-5
excerpt: '`Keywords: RAG, Knowledge Management, Hybrid Search, Agent Workflows, LLM, FAISS, University Regulations, NLP`'
date: 2025-11-07
venue: '2025년 대한산업공학회 추계학술대회'
paperurl: 'https://www.dbpia.co.kr/journal/articleDetail?nodeId=NODE12484420'
citation: '<strong>Jang, H.</strong>, & Kim, Y*. (2025). &quot;Development of an Intelligent Organizational Knowledge Management System using Hybrid Search and Agent Workflows.&quot; <i>2025년 대한산업공학회 추계학술대회</i>, 3015-3025.'
---

# Abstract
대학의 규정집은 방대하고 조항이 세분화되어 있어, 특정 상황에 맞는 규정을 신속히 찾기가 어렵다. 행정직원들이 반복적으로 규정을 확인하고 해석하는 과정에서 많은 시간이 소요되고, 업무 효율성이 떨어지며, 직원 간 해석 차이로 인해 동일한 사안에 대해 다른 답변이 나오는 경우가 발생한다. 본 연구에서는 검색증강생성(RAG) 기반 AI 에이전트를 활용하여 경희대학교 규정, 학부/대학원 시행세칙, 학사제도 등에 대한 질의응답 시스템을 개발하였다. FAISS Vector DB와 GPT-4를 활용한 하이브리드 검색 파이프라인을 구축하고, JSON 기반 구조화 전처리를 통해 검색 정확도를 향상시켰다.

<br/>

# Presentation
<iframe src="/files/presentation1.pdf#toolbar=0&navpanes=0&scrollbar=0" width="800" height="450" style="display: block; margin: auto; border: none;"></iframe>

<br/>

# Key Results

| Metric | Before | After | Improvement |
|--------|--------|-------|-------------|
| Faithfulness (RAGAS) | 0.36 | 0.52 | +44% |
| 행정 처리시간 | - | - | -45% |
| 업무효율성 | - | - | +43% |
| 학생 월간 처리시간 | 10.6h | 3.8h | -64% |

<br/>

# Key Contributions
- **RAG Pipeline:** 문서 수집 → 전처리(JSON) → FAISS 인덱스 → History-Aware RAG → Admin 콘솔까지 운영 파이프라인 구축
- **Structured Preprocessing:** PDF, HWP 등의 파일을 unstructured.io 라이브러리를 활용해 구조 기반 분할 및 메타데이터 추출
- **Hybrid Search:** FAISS Vector DB 기반 유사도 검색과 문맥적 검색을 결합한 하이브리드 검색 시스템
- **Admin Console:** 질문/답변 로그, 성능 평가(RAGAS), 피드백 확인, 부적절한 사용 감지 기능 구현
- **Source Transparency:** 출처 자동 병기, 원문 미리보기/다운로드, 코호트(연도) 인덱스로 버전 드리프트 완화

<br/>

# Methodology
- **Data Preprocessing:** HWP/PDF → JSON 변환, 구조 기반 분할 (Table, Figure 분리)
- **Embedding:** 텍스트 청크를 임베딩 모델로 벡터화 후 FAISS DB에 저장
- **Retrieval:** 유사도 기반 임베딩 문서 검색 + Rerank/Fusion으로 정확도 향상
- **Generation:** GPT-4 + Prompt Engineering으로 답변 생성

<br/>

# Acknowledgement
본 연구는 정부(과학기술정보통신부)의 재원으로 정보통신기획평가원의 지원을 받아 수행된 연구임 (No.RS-2022-00155911, 인공지능융합혁신인재양성(경희대학교)).
