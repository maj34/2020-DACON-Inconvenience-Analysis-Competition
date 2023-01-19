# LG 시스템 품질 변화로 인한 사용자 불편 예지 AI 경진대회
2020-DACON-Inconvenience-Analysis-Competition 

<br/>

## 1. 배경 & 목적

- 다양한 장비/서비스에서 일어나는 시스템 데이터를 통해 사용자의 불편을 예지
- ‘시스템 데이터’와 ‘사용자 불편 발생 데이터’를 분석하여 불편을 느끼는 원인 분석
- 평가 지표: AUC

<br/>

## 2. 주최/주관 & 참가 대상 & 성과

- 주최: LG AI Research
- 주관: DACON
- 참가 대상: 일반인, 학생 등 누구나
- 성과: 상위 12%

<br/>

## 3. 대회 기간

- 제출마감: 2021년 02월 03일
- 코드 평가 마감 및 최종순위 발표: 2021년 02월 24일

<br/>

## 4. 내용

&nbsp;&nbsp;&nbsp;&nbsp; ‘시스템 데이터’와 ‘사용자 불편 발생 데이터’를 통해 ‘사용자가 불만을 느낄 확률을 예측’하는 분류 문제이다. 변수를 크게 Error Data와 Quality Data, Problem Data 3가지로 나누어 각각의 특성에 따라 **EDA 및 피처 엔지니어링**을 진행했다. 

&nbsp;&nbsp;&nbsp;&nbsp; 피처 생성 이후에는 그 안에서 의미 있는 데이터를 선정하고 가공하고자 다양한 전처리 방법을 거쳤다. 예측력을 방해할 수 있는 **다중공선성**을 제거하고 **주성분분석, 정규화, 표준화, 피처 셀렉션**을 거쳐서 최종적으로 피처를 선정하였다.

&nbsp;&nbsp;&nbsp;&nbsp; 모델링은 LR, Catboost, KNN, XGB, LR, RF 등 여러 가지 모델을 Selection하며 실험해 보았으며 **Averaging 및 Stacking 앙상블** 과정을 거쳤다. 그 과정에서 각 모델을 Bayesian Optimization을 통해 튜닝한 결과 성능이 가장 잘 나오는 **KNN, RF, GBM, XGB, LGBM, Catboost 모델을 Stacking** 한 결과가 가장 성능이 높게 나와 해당 모델을 가지고 최종 서브미션을 구하였다.

<br/>

## 5. Process

### ch.1 Feature Engineering

- Error Data
- Quality Data
- Problem Data

---

### ch.2 Preprocessing

- Feature Correlation
- PCA
- Normalization
- Standardization
- Feature Selection

---

### ch.3 Modeling

- Model Selection
- LGBM
- Catboost
- KNN
- XGB
- Logistic Regression
- Random Forest

---

### ch.4 Ensemble

- Averaging
- Stacking

<br/>

## 6. 참고자료

[시스템 품질 변화로 인한 사용자 불편 예지 AI 경진대회 ](https://dacon.io/competitions/official/235687/overview/description)
