## 왜 Causal ML?
* ML은 데이터의 최적화되어있음
* **What if** 문제에 대한 대답 X
    * A를 B로 만들면 어떻게 될까? 더 좋아질까?
* ML은 인과관계를 알려주지 않
* ML은 결정 가능한 통찰력 제공 X


## 인과관계를 어떻게 평가하는가?
1. Randomized Controlled Trial(RCT)
* Average Treatment Effect (ATE)
* random treetment 효과를 위해서 cofounders(X)를 Treatment(T)에서 제거한다.
* 단점
    * 일부 상황에서 사용 X
    * heterogenous effect 찾지 X (이질적인 효과? 찾지 X)

2. Controlling Confounders (Unconfoundedness)
* Conditional Average Treatment Effect (CATE)
* Cofounder(X)에서 treetment 효과를 평가한다

3. Instrumental Variables (IV)
* Local Average Treatment Effect (LATE)
* Treetment에 직접적인 결과를 미치지는 않지면 영향을 미치는 randomized variable 사용

![image](https://github.com/hkyoo52/Causal-Inference/assets/63588046/a0f6a0b5-69f1-4543-a150-e321bb8e0789)

조건
1. Identification assumptions O => treetment와 결과 사이에 기본 가정 조
    * treetment와 결과 사이에 인과관계 O
    * treetment와 결과 사이에 혼란변수 X
    * treetment와 결과 사이에 시간 순서 O
    * treetment와 결과 사이에 다른 변수로 제어 O
2. treetment effect를 분리 O


## CATE Estimation with ML
* Meta-learning은 out-of-the-box ML 모델 활용
* Double/Orthogonalized Learning은 propensity score p(T|X)와 outcome model 사용
* Tree Based Model은 CART/RF 사용
* Neural Net Based Models은 동일한 layer로 control과 treetment 동시 진






https://docs.google.com/presentation/d/1lJO4Xs2YRV1Cx5UDeJ4cH8Rjc4PrAbU7QeNxfaHfPXI/edit?pli=1#slide=id.g5d7aa4ed0a_6_198
