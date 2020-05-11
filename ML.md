# Machine Learning

### 퍼셉트론 perceptron

입력값 x와 가중치 w 가 만나서 y

[이거보고 공부해야지](https://wikidocs.net/24958)
[텐서플로우](http://hunkim.github.io/ml/)


ubuntu
nvidia
cuda
cuDNN

<br>

### 책
* 밑바닥부터 시작하는 딥러닝1, 2
* 케라스 창시자에게 배우는 딥러닝
* 모두를 위한 딥러닝 -youtube

* 케라스 3분 딥러닝
* 딥러닝 입문 doit
* 판다스입문 doit
* 실체가 손에 잡히는 딥러닝
* 핸즈온 머신러닝 1, 2
* 신경망 첫걸음

<br>


퍼셉트론<br>
입력층 -> 은닉층 -> 출력층

linear<br>
saturated linear<br>
hyperbolic tangent<br>
gaussian

활성화 함수
<br>
* step(  step ---> sigmoid   )
* sigmoid (step에서 업그레이드 1과 0 사이
* hyperbolic tangent (음수도 필요한 경우
* ReLU (0보다 작으면 0으로 친다.
* 항등함수




계단함수
```python
def step_function(x):
  if x>0: 
    return 1;
  else: 
    return 0;

def step function(x):
  return np.array>0, dtype = np.int
```

float 16 반정도 float 32 단정도 float 64 배정도<br>

sigmoid vs step
신경망에서는 실


#### WX vs XW

Theory
H(x) = Wx + b

Implementation(TensorFlow)
H(X) = XW


#### softmax

logistic regression 구분하는 선을 찾는 것?
0-1사이의 값
전체의sum은 1
확률로 본다
argmax(one - hot encoding)

지수함수여서 overflow가 발생할 수 있다.
큰값으로 뺀다 데이터의 상대적 거리는 변화가 없다 뭔말이닞 모르겠다 왜 큰 값으로 뺄까 작은 값으로 빼면 안되는걸까 큰 값으로 빼면 마이너스로 내려가는거 아닌가

소프트맥스는 마지막 출력전에 사용

cost function : cross - entropy 엔트로피 읽고싶다

정답이 맞으면 0, 틀리면 무한대

optimizer: 가중치를 새로운 가중치로 업데이트!!!
cost가 제로가 될 때 까지 반복.


### layer
(은닉층

벡터데이터 2D - 완전 연결층 (fully connected), 밀집층(densely)<br>
              - 크기: samples, features<br>
시계열 or 시퀀스 3D - 순환층(recurrent:LSTM)<br>
                    - 크기 : samples, timesteps, features<br>
이미지 4D - 2D 합성곱(convolution)<br>
              - 크기 : samples, height, weight, channel<br>
                      samples, channel, height, weight<br>
동영상 5D -<br>
          -크기: samples, frames, height, weight, channel<br>
                 samples, frames, channel, heigth, weight<br>
                 
같은 말
행, 열<br>
샘플축, 특성축<br>
sample axis, feature axis<br>


np.dot vs np.matmul
<br>
a.shape 234 b.shape 243<br>
matmul(a,b).shape 233<br>
dot(a,b).shape 2323<br>

fully connected layer 완전 연결 계층



오차 역전파 backward propagation

<br>
imaga<br>
높이 너비 컬러(3RGB, 1gray)<br>
배치 (batch) 32~512
<br>
Directed Acycle Graph DAG
<br>
loss& optimizer


Keras 모든 종류의 딥러닝 모델
<br>
cpu qpu api cnn rnn ......

