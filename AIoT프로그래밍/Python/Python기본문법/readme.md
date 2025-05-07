# 🐍 파이썬 기본 문법 정리

파이썬은 문법이 간단하고 직관적이라 AIoT, 데이터 분석, 웹 개발 등 다양한 분야에서 널리 사용됩니다. 아래는 핵심적인 기본 문법입니다.

---

## 1. 변수와 자료형

```python
x = 10        # 정수
y = 3.14      # 실수
name = "AIoT" # 문자열
is_ready = True # 불린 (참/거짓)
```

---

## 2. 기본 자료형

```python
# 리스트
fruits = ["apple", "banana", "orange"]

# 튜플 (수정 불가)
point = (3, 4)

# 딕셔너리 (키-값 쌍)
person = {"name": "Kim", "age": 20}

# 집합 (중복 제거)
unique_nums = {1, 2, 3, 3}
```

---

## 3. 조건문

```python
age = 20

if age >= 18:
    print("성인입니다")
elif age >= 13:
    print("청소년입니다")
else:
    print("어린이입니다")
```

---

## 4. 반복문

```python
# for 문
for i in range(5):
    print(i)

# while 문
count = 0
while count < 5:
    print(count)
    count += 1
```

---

## 5. 함수 정의

```python
def greet(name):
    print(f"안녕하세요, {name}님!")

greet("홍길동")
```

---

## 6. 클래스 (객체지향 기초)

```python
class Car:
    def __init__(self, name):
        self.name = name

    def drive(self):
        print(f"{self.name}가 달립니다.")

my_car = Car("소나타")
my_car.drive()
```

---

## 7. 예외 처리

```python
try:
    x = 10 / 0
except ZeroDivisionError:
    print("0으로 나눌 수 없습니다.")
finally:
    print("프로그램 종료")
```

---

## 8. 파일 입출력

```python
# 파일 쓰기
with open("example.txt", "w") as f:
    f.write("AIoT 반도체 설계 과정")

# 파일 읽기
with open("example.txt", "r") as f:
    content = f.read()
    print(content)
```

---

## 9. 외부 라이브러리 사용

```python
import math
print(math.sqrt(16))  # 제곱근

import random
print(random.randint(1, 10))  # 1~10 사이 랜덤 정수
```

---

## 📌 참고
- 들여쓰기가 문법에 포함됩니다 (보통 4칸).
- 변수 선언 시 타입을 명시하지 않아도 됩니다.
- 주석은 `#` 또는 `` 사용

