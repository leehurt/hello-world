# 회귀분석의 간단한 실습
# scikit-learn : 파이썬 기반의 머신러닝 및 데이터 분석을 위한 오픈 소스 라이브러리
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression

# 공부시간 : 독립변수, 시험점수 : 종속변수
x = [[2],[4],[6],[8],[10]]       # 공부시간
y = [[81],[93],[90],[97],[100]]  # 시험점수

# 산점도 그래프
plt.scatter(x, y)
plt.show()

# 학습시키기
model = LinearRegression()      # 선형회귀분석 객체 생성하기

# 선형회귀분석 객체를 이용하여 학습시키기
model.fit(x, y)

# 예측하기
result = model.predict([[7]])   # 7시간 공부
print(f'예상점수:{result}')
