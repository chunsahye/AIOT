# 🐼 Pandas 기본 문법 정리

Pandas는 데이터프레임(DataFrame)이라는 구조를 사용하여, 행과 열로 이루어진 데이터를 효율적으로 처리하고 분석할 수 있도록 도와주는 Python 라이브러리입니다.

---

## 1. Pandas 임포트

```python
import pandas as pd
```

---

## 2. 데이터 생성

```python
# 딕셔너리로부터 DataFrame 생성
data = {
    '이름': ['철수', '영희', '민수'],
    '나이': [25, 30, 28],
    '도시': ['서울', '부산', '대구']
}

df = pd.DataFrame(data)
```

---

## 3. CSV 파일 읽기 / 저장

```python
# 파일 읽기
df = pd.read_csv('data.csv')

# 파일 저장
df.to_csv('output.csv', index=False)
```

---

## 4. 데이터프레임 정보 확인

```python
df.head()         # 처음 5행 보기
df.tail()         # 마지막 5행 보기
df.shape          # (행, 열) 크기
df.columns        # 컬럼 이름
df.info()         # 데이터 타입 및 결측치 정보
df.describe()     # 수치형 데이터 요약 통계
```

---

## 5. 데이터 선택 (인덱싱)

```python
# 열 선택
df['이름']                # Series
df[['이름', '나이']]       # DataFrame

# 행 선택 (인덱스로)
df.loc[0]                # 라벨 기반
df.iloc[0]               # 위치 기반
```

---

## 6. 필터링 (조건)

```python
# 나이가 28 이상인 사람
df[df['나이'] >= 28]

# 서울에 사는 사람
df[df['도시'] == '서울']
```

---

## 7. 정렬

```python
df.sort_values(by='나이')                # 오름차순 정렬
df.sort_values(by='나이', ascending=False)  # 내림차순 정렬
```

---

## 8. 데이터 추가 및 수정

```python
# 열 추가
df['점수'] = [85, 90, 95]

# 행 추가
new_row = pd.DataFrame([['지수', 27, '광주', 88]], columns=df.columns)
df = pd.concat([df, new_row], ignore_index=True)

# 값 수정
df.at[0, '나이'] = 26
```

---

## 9. 결측치 처리

```python
df.isnull()                # 결측값 여부 확인
df.dropna()                # 결측값이 있는 행 삭제
df.fillna(0)               # 결측값을 0으로 대체
```

---

## 10. 그룹화 및 집계

```python
df.groupby('도시')['나이'].mean()     # 도시별 평균 나이
df.groupby('도시').agg({'나이': 'max', '점수': 'mean'})
```

---

## 참고
- Pandas는 데이터 전처리, 통계 분석, 시각화 등 다양한 작업에 필수적입니다.
- 실무에서는 Pandas와 함께 NumPy, Matplotlib, Seaborn 등을 함께 사용합니다.

