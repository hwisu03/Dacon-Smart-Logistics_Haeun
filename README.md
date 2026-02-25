# 🚢 Dacon-Smart-Logistics_Haeun

### 📌 프로젝트 개요
- **목표:** 선박 운항 데이터의 이상치(Outlier) 탐색 및 정제
- **데이터셋:** 데이콘(DACON) 스마트 해운 경진대회 데이터
- **성과:** 통계적/물리적 근거 기반의 데이터 무결성(Data Integrity) 확보

### 🛠️ 사용 기술 및 분석 전략
- **Library:** Pandas, Matplotlib, Scikit-learn, Folium
- **Analysis Strategy:**
  - **Statistical:** IQR(Interquartile Range) 및 Z-Score 기반의 단변량 이상치 제거
  - **Domain:** 선박의 물리적 한계치(최대 속도, 가속도 등)를 반영한 필터링
  - **Advanced:** Isolation Forest 모델을 활용한 다변량 이상 탐지
  - **Preprocessing:** 선형 보간법(Linear Interpolation)을 이용한 결측치 보정

### 📈 실험 결과
- **성과:** 센서 노이즈 제거를 통한 운항 궤적(Trajectory) 정상화 및 데이터 품질 향상
- **활용:** 정제된 데이터를 바탕으로 도착 예정 시간(ETA) 예측의 정확도 기틀 마련
