# Ensemble---Boosting-Stacking

## Boosting - 부스팅
![부스틴 기본 이론 사진](https://github.com/zzzxxcc123/Ensemble---Boosting-Stacking/assets/117971016/79242355-78e2-4905-ab56-c254be486453)
1. 부스틴(Boosting)은 Bagging랑 크게 다르지는 않으며, 거의 동일한 매커니즘을 갖고 있습니다
2. 다른점은, Bagging은 각각 분류기를이 학습시 독립성을 유지하면서 끝난후 결과를 종합하는 가법
3. Boosting은 이전 분류기의 학습 결과를 토대로 다음 뷴류기의 학습 데이터의 샘플을 가중치를 조정하며 학습을 진행 시키는 방법
4. Boosting의 장점은 오답에 다한 높은 가중치를 주텨하므로 정확도가 높게 나타난다
5. **XGBoost , AdaBoost, GradientBoost, lightGBM**

