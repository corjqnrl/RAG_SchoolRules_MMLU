# RAG_SchoolRules_MMLU

이 프로젝트는 **Upstage(Solar) 기반 LLM**을 활용하여, **직접 학습(Fine-tuning) 없이** 다양한 기법을 적용해 **벤치마크 성능을 향상**시키는 것을 목표로, 프롬프트 엔지니어링, RAG, Upstage API 활용 등의 방법으로 모델의 응답 품질을 개선합니다.

---

## 📌 Overview

* Upstage에서 제공하는 **Solar LLM**을 포함한 다양한 모델을 백본(backbone)으로 사용 가능
* **Fine-tuning 금지** (직접 학습 불가)
* 프롬프트 설계, 다중 턴 상호작용, RAG, 외부 API 연계 등 **추론 단계 개선 기법**을 중심으로 성능 향상
* 최종 출력은 **자동 채점/파싱이 가능하도록 직접 파싱 가능한 형태**여야 함

📄 [프로젝트 보고서 (PDF)](docs/NLP_project.pdf)

---

## 🗓️ Dates

* **프로젝트 기간:** 11/5 - 12/8

---

## ✅ Requirements

### 1. Backbone LLM

* Upstage **Solar**를 포함하여 **모든 종류의 LLM 사용 가능**
* 사용한 모델의 **Model Card 명시 필수**

### 2. Prompt Engineering

* 추가적인 **프롬프트 엔지니어링** 및 **시스템/지시 프롬프트** 사용 가능
* 다중 턴(Multi-turn) 전략 허용
* 단, **최종 답변은 단일 출력으로 직접 파싱 가능**해야 함

📎 참고 튜토리얼:

* `prompt_engineering_tutorial.ipynb`

---

### 3. Upstage API 활용

다음 Upstage API들을 활용

* Chat API
* Embeddings API
* Document Parse API
* 기타 Upstage에서 제공하는 API

📎 참고 문서:

* [https://developers.upstage.ai/docs/apis/chat](https://developers.upstage.ai/docs/apis/chat)

---

### 4. Retrieval-Augmented Generation (RAG)

* 외부 지식을 활용한 **RAG 방식 허용**
* Embedding API를 이용해 **자체 Knowledge Base(KB)** 구축 가능

⚠️ **주의 사항**

* **테스트셋과 직접적으로 연관된 데이터 수집은 부정행위(치팅)**로 간주

  * 예: MMLU-pro 평가에서 MMLU 또는 MMLU-pro 데이터를 KB로 사용하는 경우

📎 참고 튜토리얼:

* `RAG_tutorial.ipynb`

---

### 5. 제한 사항

* ❌ **Reasoning Model 사용 금지**
* ❌ Fine-tuning 금지
* ✅ **Chat Mode만 사용 가능**
* ✅ 다중 턴 추론 과정은 허용되나, **최종 출력은 정형화된 단일 응답**이어야 함

---

## 📊 Evaluation

* 주어진 벤치마크에 대해 **정확도** 평가
* 개선 전/후 성능 비교

---

## 👥 Team

* 팀원: 3명

---

## 📄 License

본 프로젝트는 교육 목적의 프로젝트이며, Upstage API 및 모델 사용 약관을 따릅니다.

---

## 🔗 References

* Upstage Official Website: [https://www.upstage.ai](https://www.upstage.ai)
* Upstage Developers Docs: [https://developers.upstage.ai](https://developers.upstage.ai)

---


