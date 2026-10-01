<h1 align="center">안녕하세요, 조수빈입니다. 👋</h1>
<h3 align="center">데이터를 통해 문제를 정의하고 해결하는 데이터·AI 직무를 준비하고 있습니다.</h3>

<p align="center">
  <em>"정확도가 아니라 목적에 맞는 지표를, 모델이 아니라 데이터를 먼저 본다"</em>
</p>

---

## 🙋‍♀️ About Me

- 🔭 현재 **데이터 분석 / 머신러닝** 분야로의 전향을 준비하고 있습니다.
- 🌱 요즘은 **SQL(BigQuery)** 과 **퍼널·A/B 테스트 분석** 을 집중적으로 학습하고 있습니다.
- 💡 **회계 실무 7년** 경험에서 얻은 습관 — 숫자가 맞는지 확인한 뒤 다음 단계로 넘어가는 것 — 이
  분석에서도 그대로 쓰이고 있습니다. 결과가 나왔을 때 "이 숫자가 정말 맞는 근거인가"를 먼저 묻습니다.
- 🎓 **KT AICE Associate** 취득
- 📫 연락처: **sbeen0711@gmail.com**

---

## 🛠️ Tech Stack

**Language**

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)

**Data & ML**

![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=for-the-badge&logo=scipy&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-337AB7?style=for-the-badge&logo=python&logoColor=white)

**Deep Learning & NLP**

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-D00000?style=for-the-badge&logo=keras&logoColor=white)
![HuggingFace](https://img.shields.io/badge/🤗%20Transformers-FFD21E?style=for-the-badge&logoColor=black)

**Visualization & Tools**

![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=python&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-444876?style=for-the-badge&logo=python&logoColor=white)
![Colab](https://img.shields.io/badge/Google%20Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

---

## 📊 Featured Projects

### 1. 은행 신용카드 고객 이탈 예측 &nbsp;·&nbsp; `이진 분류`

고객 이탈 가능성을 사전에 식별해 이탈 방지 대상을 선별하는 프로젝트입니다.

이탈 고객이 전체의 16%에 불과한 불균형 데이터였습니다. 모든 고객을 "유지"로 예측해도
정확도가 84%에 도달하므로, **정확도가 아니라 재현율을 우선 지표로 설정**했습니다.

| 지표 | Baseline | 개선 모델 |
|---|---|---|
| 재현율 (이탈) | 0.70 | **0.83** |
| 미탐지 이탈 고객 | 147명 | **85명** |

정확도를 0.29%p 희생하는 대신 이탈 고객 62명을 추가로 포착했습니다.

**사용 기술** : Python, Pandas, scikit-learn, SciPy, Seaborn
🔗 [프로젝트 보러가기](https://github.com/senube-data/credit-card-churn-prediction)

---

### 2. 지역 연평균 기온 예측 &nbsp;·&nbsp; `회귀`

기후·대기오염 데이터를 결합해 지역별 연평균 기온을 예측하는 프로젝트입니다.

세 모델의 성능이 모두 낮게 나왔을 때, 모델을 추가하는 대신 **입력 변수를 다시 검토**했습니다.
전처리 단계에서 "단순 식별 번호"로 판단해 삭제했던 `LocationID`가
실은 위도와 기후대를 담은 가장 중요한 정보였습니다.

| 지표 | 기존 | LocationID 복원 |
|---|---|---|
| MAE | 2.71 | **1.80** (33% 감소) |
| R² | 0.09 | **0.61** |

모델과 하이퍼파라미터는 전혀 바꾸지 않고, 변수 하나를 되살린 것만으로 얻은 결과입니다.

**사용 기술** : Pandas, scikit-learn, TensorFlow/Keras, Matplotlib, Seaborn
🔗 [프로젝트 보러가기](https://github.com/senube-data/climate-temperature-prediction)

---

### 3. 대출 상환 가능성 점수 예측 &nbsp;·&nbsp; `회귀 · 모델 해석`

신청자의 개인 정보와 금융 이력으로 상환 가능성 점수(0~100)를 예측합니다.
대출 심사는 결과의 근거를 설명할 수 있어야 하는 영역이므로, 예측 성능과 함께
**해석 가능성**을 검증 목표로 삼았습니다.

가장 단순한 LinearRegression이 XGBoost·RandomForest·딥러닝보다 좋은 성능을 냈습니다.
**MAE 5.67** — 검증 데이터 표준편차 14.47 대비 오차를 61% 줄인 수치이며, **R² 0.729** 입니다.

결측치 대치를 데이터 분리 **이후로** 옮겨 검증 데이터 정보가 새어 들어가는 것을 차단했고,
선형 회귀 계수와 XGBoost 변수 중요도를 교차 확인해 결과의 신뢰도를 높였습니다.

**사용 기술** : Pandas, scikit-learn, XGBoost, TensorFlow/Keras, Matplotlib, Seaborn
🔗 [프로젝트 보러가기](https://github.com/senube-data/loan-repayment-prediction)

---

### 4. 딥러닝 실습 노트북 — 결과를 검증하는 연습 &nbsp;·&nbsp; `CV · NLP · 진단`

딥러닝 실습 5건을 출발점으로, **"돌아갔다"에서 멈추지 않고 결과가 맞는지 확인한** 기록입니다.
5건 중 2건에서 **에러 없이 돌아가지만 결과가 잘못된 상태**를 발견하고 원인을 추적해 수정했습니다.

| 노트북 | 주제 | 핵심 발견 |
|---|---|---|
| SMILES 화학식 토큰화 | 토큰화 | 대괄호 표기(`[C@@H]`)가 단일 토큰으로 보존되어 입체화학 정보가 유지됨을 검증 |
| 레스토랑 팁 EDA | 통계 분석 | 팁 **금액**은 결제금액과 양의 상관(r=0.68), 팁 **비율**은 음의 상관(r=−0.34) |
| ViT 전처리 버그 추적 | 원인 진단 | 전처리 이중 적용으로 모델이 모든 이미지를 동일하게 인식하던 문제 발견·수정 |
| 이미지 분류 기준선 설계 | 성능 평가 | 정확도 91%를 평균 RGB 로지스틱 회귀 기준선과 비교해 재해석 |
| LLM 디코딩 전략 비교 | 생성 제어 | 반복 현상의 원인이 모델 크기가 아닌 `do_sample=False` 기본값임을 확인 |

가장 공들인 것은 **ViT 전처리 버그 추적**입니다. 파인튜닝된 모델이 테스트 이미지 10장 중
9장을 같은 클래스로 예측했는데, 클래스별 logit의 **이미지 간 표준편차**를 측정해
"모델이 모든 입력을 같은 것으로 보고 있다"는 사실을 먼저 입증하고 전처리 단계로 거슬러 올라갔습니다.

```
ToTensor()         : 0~255  ->  0~1        (255로 나눔)
ViTImageProcessor  : 0~1    ->  0~0.0039   (255로 또 나눔)  ← do_rescale=True 기본값
```

에러는 한 번도 발생하지 않았습니다. 코드는 정상 종료되었고 결과만 틀렸습니다.

**사용 기술** : PyTorch, HuggingFace Transformers, scikit-learn, SciPy, Seaborn
🔗 [프로젝트 보러가기](https://github.com/senube-data/Deeplearning)

---

## 🔍 네 프로젝트를 관통하는 것

다루는 데이터도 문제 유형도 달랐지만, 같은 질문을 반복했습니다.
**지금 보고 있는 숫자가 정말 맞는 근거인가.**

| | 묻지 않은 것 | 실제로 물은 것 |
|---|---|---|
| **이탈 예측** | 정확도가 높은가 | 무엇을 성공으로 볼 것인가 |
| **기온 예측** | 어떤 모델이 나은가 | 입력 변수가 충분한가 |
| **대출 점수** | 오차가 작은가 | 무엇과 비교한 오차인가 |
| **딥러닝 검증** | 코드가 돌았는가 | 모델이 실제로 데이터를 보고 있는가 |

회계 현장에서 7년간 숫자가 맞는지 확인한 뒤 다음 단계로 넘어가던 습관이
분석에서도 같은 방식으로 쓰이고 있다고 생각합니다.

---

## 📫 Contact

[![Email](https://img.shields.io/badge/sbeen0711@gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:sbeen0711@gmail.com)
[![GitHub](https://img.shields.io/badge/github.com/senube--data-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/senube-data)


