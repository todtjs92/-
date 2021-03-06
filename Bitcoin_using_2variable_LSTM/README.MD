# 비트코인시세예측하기: 금을 활용한 이변량 LSTM 모델

비트코인시세를 예측하는데 있어 단순히 비트코인의 과거시세만을 이용하는 것이 아니라 비트코인과 상관성이 높은
투자자산들( 주식, 금, 달러)을 이용하면 성능을 높일 수 있을 것이라고 생각하였다.
#### 1.시계열 데이터에서 DTW를 이용하여 상관성을 구할것을 제시
비트코인과의 상관성을 확인하는 과정에서 기존의 상관계수를 통한 방식 대신 시계열데이터에서 DTW를 이용하여
상관성을 구할 것을 제시하였다. 상관계수는 두 데이터 간의 선형성만을 보여주기 때문에 시계열데이터에서 추세를
비교하기에는 적합하지 않지만 DTW는 추세를 고려하여 비교를 하기 때문에 더 좋은 비교방법이라고 할 수 있다.
실제로 DTW방법으로 비교했을때 비트코인과 유사성이 가장 높았던 금을 이용하여 이변량 LSTM을 만든결과
가장 좋은성능을 보였다.
#### 금이 DTW방식으로 비교했을때 가장 비트코인과 유사했음 (1위,2위, 3위 표시한것)
![순위](https://user-images.githubusercontent.com/59354220/102011427-502df300-3d87-11eb-9371-cce66c4cdc1a.png)
## DTW ( https://en.wikipedia.org/wiki/Dynamic_time_warping)
![DTWgrid](https://user-images.githubusercontent.com/59354220/102012611-b5d1ad80-3d8e-11eb-8008-41c8c5dbf295.gif)
##  최종모델 예측결과
### 금을 활용하여 모델을 만들었을때 MSE값이 가장 낮게나옴
![다른 모델과 비교](https://user-images.githubusercontent.com/59354220/102011429-51f7b680-3d87-11eb-8db7-5a1ecf34a5ea.png)
### 예측한 시세와 실제 시세 비교
![예측결과](https://user-images.githubusercontent.com/59354220/102010882-3c34c200-3d84-11eb-9500-1872f831bd37.png)