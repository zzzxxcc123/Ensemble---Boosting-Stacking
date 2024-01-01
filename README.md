# Ensemble---Boosting-Stacking

## Boosting - 부스팅
![부스틴 기본 이론 사진](https://github.com/zzzxxcc123/Ensemble---Boosting-Stacking/assets/117971016/79242355-78e2-4905-ab56-c254be486453)
1. 부스틴(Boosting)은 Bagging랑 크게 다르지는 않으며, 거의 동일한 매커니즘을 갖고 있습니다
2. 다른점은, Bagging은 각각 분류기를이 학습시 독립성을 유지하면서 끝난후 결과를 종합하는 가법
3. Boosting은 이전 분류기의 학습 결과를 토대로 다음 뷴류기의 학습 데이터의 샘플을 가중치를 조정하며 학습을 진행 시키는 방법
4. Boosting의 장점은 오답에 다한 높은 가중치를 주텨하므로 정확도가 높게 나타난다
5. **XGBoost , AdaBoost, GradientBoost, lightGBM**

## Stacking - 스태킹
앙상블은 여러 모델을 조합하여 단일 모델보다 더 강력한 예측 성능을 달성하는 기법입니다. 스태킹(Stacking)은 앙상블의 한 형태로, 여러 모델을 조합하는 방식 중 하나입니다. 스태킹은 다양한 모델들이 각자의 예측을 생성하고, 이 예측들을 다시 하나의 메타 모델이라 불리는 모델에 입력으로 사용하여 최종 예측을 수행합니다.

스태킹은 일반적으로 다음과 같은 단계로 진행됩니다:
1. **원본 데이터셋 분할:** 데이터셋을 훈련용(train)과 테스트용(test)으로 나눕니다.
2. **기본 모델 훈련:** 여러 다른 기본 모델들을 각각 훈련시킵니다. 이 모델들은 동일한 데이터셋을 기반으로 각기 다른 특징들을 학습하게 됩니다.
3. **기본 모델 예측 생성:** 각 기본 모델은 테스트 데이터셋에 대한 예측을 생성합니다.
4.** 메타 모델 훈련:** 기본 모델들이 생성한 예측을 입력으로 받아, 최종 예측을 수행할 메타 모델을 훈련합니다. 이 메타 모델은 각 기본 모델의 예측을 학습하여 최적의 가중치를 찾게 됩니다.
5. **최종 예측 수행:** 메타 모델에 기본 모델들의 예측을 입력으로 주어 최종 예측을 수행합니다.

### 장점
1. 다양한 모델의 장점을 결합하여 성능을 향상시킬 수 있다

### 단점
1. 모델을 여러 개 사용하면 복잡성이 증가하고, 과적합(overfitting)의 위험이 있다

그래서 CV(교차검증)을 많이 사용한다
