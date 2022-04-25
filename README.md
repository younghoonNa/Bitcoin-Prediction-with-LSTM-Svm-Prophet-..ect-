# Machine_Leraning & RNN_LSTM - Bitcoin-Price-Production
## 머신러닝과 & 딥러닝을 이용한 가상화페 예측 프로그램 <br>
 <img width="40%" src="https://user-images.githubusercontent.com/38518648/145906341-6af853f6-c2c1-419c-9b4f-851b70c71366.png"/>

<br>
<br>

### 주요 예측방법.
1. LSTM
2. Prophet 모델 사용

``` python:
!pip install fbprophet
!pip install pyupbit
from keras.layers import LSTM
from fbprophet import Prophet
import pyupbit
```

### 업비트 API 발급
- 업비트 API 발급하기 [링크](https://upbit.com/mypage/open_api_management)
- 카카오톡 인증 후 발급 가능.
- access_key, secret_key 발급 후 기입.
``` python:
access_key = "your_Access_key"
secret_key ="Secret_key"
```

<br>

### 코인 종목 고르기
- KRW-BTC(비트코인) -> KRW-DOGE (도지코인) 등 다양한 코인 예측 가능. <br> 
- 코인 이름은 [업비트 링크](!https://upbit.com/exchange?code=CRIX.UPBIT.KRW-BTC) 에서 본인이 예측하고자 하는 코인 이름 적기.
- get_ohlcv를 조정하여 월봉, 분봉을 통한 예측 가능.
``` python:
#업비트에서 가격을 가져오는 get_ohlcv 함수 사용. 
df = pyupbit.get_ohlcv("KRW-BTC", count = time+10, period=0.01)
```

### 성능
- LSTM 및 Prophet 사용을 통해 하루 평균 1~2% 의 수익을 보임.


2021년 12월 13일 기준<br>
Model : Prophet <br>
2022년 12월 예측 가격 : 1억 500만   (최소 8천 3백만, 최대 1억 2천)<br>
2026년 12월 예측 가격 : 2억 2천만   (최소 1억, 최대 3억 5천)<br>

---
비트코인 예측 
<p>
  <img width="48%" src="https://user-images.githubusercontent.com/38518648/145815952-fd8afbd1-a1fd-4849-9d0a-e4c038fceca7.png"/>
  <img width="48%" src="https://user-images.githubusercontent.com/38518648/145816128-d035845e-20b4-401c-940b-9e48754250b5.png"/>
</p>

---
도지코인 예측
<p>
  <img width="48%" src="https://user-images.githubusercontent.com/38518648/145816015-431280d9-5a3c-4d9a-ba83-8283d118ba94.png"/>
  <img width="48%" src="https://user-images.githubusercontent.com/38518648/145815973-99c43edf-a4d2-4a1c-aac7-d1a732c4b8fa.png"/>
  <img width="48%" src="https://user-images.githubusercontent.com/38518648/145815990-57ec9163-4292-4da2-93b6-961ee0c33b09.png"/>
  <img width="48%" src="https://user-images.githubusercontent.com/38518648/145816895-badbe070-4574-4703-a613-95cf3929020b.png"/>

</p>
