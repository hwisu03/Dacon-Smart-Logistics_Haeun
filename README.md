# 🚢 Smart-Logistics: Maritime Outlier Detection (DACON)

### 📌 프로젝트 개요 (Overview)
- **주제:** 선박 운항 데이터를 활용한 이상치(Outlier) 탐색 및 정제
- **데이터셋:** 데이콘(DACON) 스마트 해운 경진대회 데이터
- **목표:** 해상 센서 노이즈 및 비정상 운항 데이터를 식별하여 데이터 무결성(Data Integrity) 확보

---

### 📊 사용된 통계 및 분석 기법 (Methodology)

산업데이터공학적 관점에서 데이터의 분포를 분석하고, 도메인 특성에 적합한 통계적 임계치를 설정했습니다.

#### 1. 통계적 이상치 식별 (Statistical Detection)
- **IQR (Interquartile Range) Method:** 데이터의 사분위수($Q_1, Q_3$)를 활용하여 이상치에 강건한(Robust) 필터링 수행
    - **기준:** $[Q_1 - 1.5 \times IQR, Q_3 + 1.5 \times IQR]$ 범위를 벗어나는 극단치 제거
- **Z-Score Analysis:** 정규분포를 가정할 수 있는 피처에 대해 평균으로부터 $\pm3\sigma$ 이상 떨어진 노이즈 탐색

#### 2. 다변량 및 도메인 검증 (Advanced Validation)
- **Isolation Forest:** 위치, 속도, 코스 간의 복합적인 관계를 고려하여 비지도 학습 기반의 다변량 이상치 탐지
- **물리적 임계치 필터링:** 선박의 최대 항속 성능 및 물리적 가속 한계를 초과하는 센서 오류 데이터 제거

---

### 🛠️ 데이터 전처리 (Data Preprocessing)

- **EDA & Visualization:** 항적 시각화로 비정상 궤적 데이터(Anomaly) 직관적 검증
- **Missing Value Handling:** 센서 수신 불량 구간에 대해 보간법(Interpolation)을 적용하여 시계열 연속성 확보
- **Feature Engineering:** 운항 효율 및 도착 예정 시간(ETA) 예측을 위한 항행 변수 가공

---

### 🎓 전공 및 전문성 강점 (Academic Relevance)

- **산업데이터공학적 접근:** 홍익대학교 산업데이터공학 전공생으로서 데이터 품질 관리(Quality Management) 프로세스 설계
- **글로벌 역량:** 독일 대학원 진학 및 유학 포트폴리오 구성을 위해 데이터 정제 과정의 통계적 근거(Statistical Reasoning)를 구조화함
