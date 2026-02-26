# 🚢 Dacon-Smart-Logistics_Haeun

### 📌 프로젝트 개요
- **목표:** 선박 운항 데이터를 활용한 이상치(Outlier) 및 비정상 데이터 탐색
- **데이터셋:** 데이콘(DACON) 스마트 해운 경진대회 데이터
- **핵심 성과:** 다양한 Boosting 모델과 AutoML을 활용하여 이상치 탐지 성능 극대화

### 🛠️ 사용 기술 및 모델링 전략
- **Library:** Pandas, Scikit-learn, XGBoost, LightGBM, CatBoost, AutoGluon
- **Modeling Strategy:**
  - **Gradient Boosting:** XGBoost, LightGBM, CatBoost를 개별 적용하여 데이터 패턴 학습 및 이상치 식별
  - **AutoML:** **AutoGluon(TabularPredictor)**을 도입하여 단일 모델의 한계를 보완하고 최적의 앙상블(Ensemble) 조합 도출
  - **Optimization:** 하이퍼파라미터 튜닝을 통해 과적합(Overfitting) 방지 및 일반화 성능 확보

### 📈 실험 결과
- **Best Model:** AutoGluon (WeightedEnsemble) 및 CatBoost
- **성과:** 단일 모델 대비 앙상블 모델 적용 시 이상치 탐지 정확도 및 안정성 향상 확인
- **결론:** 복잡한 해상 센서 데이터에서는 다수의 모델을 결합한 Stacking/Ensemble 기법이 가장 효과적임을 입증

