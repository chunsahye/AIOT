# 📊 NumPy 기본 문법 정리

NumPy는 Python에서 다차원 배열을 처리하고, 수학적 계산을 빠르게 수행할 수 있도록 지원하는 라이브러리입니다.

---

## 1. NumPy 임포트

```python
import numpy as np
```

---

## 2. 배열 생성

```python
# 리스트를 배열로 변환
arr = np.array([1, 2, 3])

# 2차원 배열
arr2d = np.array([[1, 2], [3, 4]])

# 0으로 채워진 배열
zeros = np.zeros((3, 3))

# 1로 채워진 배열
ones = np.ones((2, 4))

# 임의의 값으로 채운 배열
rand = np.random.rand(3, 3)

# 범위로 배열 생성
arange = np.arange(0, 10, 2)

# 일정한 간격으로 배열 생성
linspace = np.linspace(0, 1, 5)
```

---

## 3. 배열 정보 확인

```python
arr.shape       # 배열 형태
arr.ndim        # 차원 수
arr.dtype       # 데이터 타입
arr.size        # 전체 원소 개수
```

---

## 4. 인덱싱과 슬라이싱

```python
arr = np.array([10, 20, 30, 40])

arr[0]          # 첫 번째 요소
arr[-1]         # 마지막 요소
arr[1:3]        # 2번째부터 3번째까지

matrix = np.array([[1, 2], [3, 4]])
matrix[0, 1]    # 첫 행 두 번째 열
```

---

## 5. 배열 연산

```python
a = np.array([1, 2, 3])
b = np.array([4, 5, 6])

a + b           # 배열 덧셈
a * b           # 원소별 곱셈
a @ b           # 행렬 곱 (또는 np.dot(a, b))

np.sum(a)       # 합계
np.mean(a)      # 평균
np.max(a)       # 최대값
```

---

## 6. 브로드캐스팅

```python
a = np.array([1, 2, 3])
a + 10          # [11, 12, 13] - 자동으로 10이 각 원소에 적용됨
```

---

## 7. 배열 재구성 및 변형

```python
a = np.arange(6)         # [0 1 2 3 4 5]
a.reshape((2, 3))        # 2행 3열로 변형

a.flatten()              # 1차원으로 평탄화

np.transpose(arr2d)      # 전치 행렬
```

---

## 8. 조건 필터링

```python
a = np.array([1, 2, 3, 4, 5])
a[a > 3]                 # [4, 5] - 조건에 맞는 값만 추출
```

---

## 9. 난수 생성

```python
np.random.seed(0)         # 난수 고정
np.random.rand(3)         # 0~1 사이 실수 3개
np.random.randint(0, 10)  # 0~9 중 하나의 정수
```

---

## 참고
- NumPy는 행렬, 벡터 연산을 매우 빠르게 처리할 수 있으며, AIoT, 데이터분석, 영상처리 등 다양한 분야에서 필수적으로 사용됩니다.
- 배열의 차원, 형상(shape)을 자유롭게 다룰 수 있는 능력이 중요합니다.

