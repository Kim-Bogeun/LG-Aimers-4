# 24-LG-Aimers-Phase2
### 📢 대회 개요
- **주제**: MQL 데이터 기반 B2B 영업기회 창출 예측 모델 개발
- **기간**: 2024.02.01 ~ 02.26 (약 4주)
- **주최**: LG AI Research
<br>

### 📝 Feature Engineering
duplicate 행 제거
Cardinality가 높은 변수와 낮은 변수에 대해 각각 다른 처리 진행   
높은 경우 : Mean target Encoding 및 smoothing   
낮은 경우 : One-hot Encoding / 데이터 확인 후 적절한 파생변수 생성   
<br>

### 📊 Modeling 
XGBoost , LGBM 하이퍼파라미터 튜닝 및 앙상블   
클래스 불균형 약 10:1 , Undersampling은 부적절하다고 판단   
과적합의 우려로 Oversampling 진행하지 않음, threshold 변경하는 방식으로 조정   
<br>

### 🏅 결과
|  | f1 score | 등수 |
| :-: | :-: | :-: |
| public | 0.765328 | 34 / 884 (상위 3.8%) |
| private | 0.767698 | 57 / 884 (상위 6.4%) |

<br>
학회 일정으로 인해 2월 15일부터 모델링을 시작했습니다. 약 상위 30팀까지 진출하는 본선에는 진출 실패했습니다.
