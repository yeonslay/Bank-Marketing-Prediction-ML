# Bank-Marketing-Prediction-ML

---

## 📘 Overview  
본 프로젝트는 은행 고객 데이터를 기반으로 **정기 예금(Term Deposit)** 가입 여부를 예측하는 머신러닝 분류 모델링입니다.  
총 **31,647명의 고객 데이터**를 활용했으며, 데이터에는 개인 정보, 신용 정보, 마케팅 활동 관련 정보가 포함되어 있습니다.  
데이터의 클래스는 **불균형(가입자 3,702명 / 미가입자 27,945명)** 으로 구성되어 있어, 모델 설계 시 이를 고려하여 평가지표는 **f1-score**로 하였습니다.

---

## Dataset

| 변수명 | 설명 | 데이터 타입 |
|--------|------|--------------|
| `ID` | 각 고객 데이터의 고유 식별자 | string |
| `age` | 고객 나이 | int |
| `job` | 직업 유형 | categorical |
| `marital` | 결혼 상태 | categorical |
| `education` | 교육 수준 | categorical |
| `default` | 신용 불량 여부 | categorical |
| `balance` | 계좌 잔고 (유로 단위) | numeric |
| `housing` | 주택 대출 여부 | categorical |
| `loan` | 개인 대출 여부 | categorical |
| `contact` | 마케팅 접촉 방식 | categorical |
| `day` | 마지막 연락 일자 | int |
| `month` | 마지막 연락 월 | categorical |
| `duration` | 마지막 통화 시간(초 단위) | int |
| `campaign` | 현재 캠페인 동안의 통화 횟수 | int |
| `pdays` | 이전 캠페인 후 경과 일수 (`-1`은 연락 없음을 의미) | int |
| `previous` | 이전 캠페인에서의 연락 횟수 | int |
| `poutcome` | 이전 캠페인 결과 | categorical |
| `label` | 정기 예금 가입 여부 (1 = 가입, 0 = 미가입) | binary |

---

## ⚙️ Modeling Pipeline  

본 프로젝트의 모델 학습 과정은 LightGBM 기반 분류 모델을 중심으로,  
데이터 전처리 → 변수 선택 → 하이퍼파라미터 튜닝 → 임계값 최적화 → 성능 평가 순으로 진행하였습니다. 자세한 사항은 코드 및 주석 참고바랍니다.
