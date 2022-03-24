# Coding Test Practice 01
---
프로그래머스 코딩테스트 연습 중 학습한 내용
> Contents
> * gcd(최대공약수), lcm(최소공배수) 함수
> * divmod 함수
> * Counter 클래스


### <strong>gcd & lcm</strong>
---
gcd 함수는 파이썬 버전 3.5에 최초로 추가됨
### math.gcd 함수
* 함수 모양
  * *math.gcd(num)*
* 함수 설명
  * gcd의 인자로 0개부터 N개까지의 숫자 입력 가능
  * gcd는 인자로 들어온 숫자들의 최대 공약수(정수)를 반환함

```python
import math # 필수
math.gcd(3) # 3 반환
math.gcd(4, 8)  # 4 반환
math.gcd(3, 6, 9) # 3 반환
```

lcm 함수는 파이썬 버전 3.9에 최초로 추가됨
### <strong>math.lcm 함수</strong>
* 함수 모양
  * *math.lcm(num)*
* 함수 설명
  * gcd의 인자로 0개부터 N개까지의 숫자 입력 가능
  * gcd는 인자로 들어온 숫자들의 최소 공배수(양의 정수)를 반환함
  * 인자가 없는 경우, 즉 math.lcm()의 반환 값은 1
  * 인자 중에 하나라도 0인 경우 반환 값은 0

*  예시 :
```python
import math # 필수
math.lcm(3) # 3 반환
math.lcm(4, 8)  # 8 반환
math.lcm(2, 3, 4) # 12 반환
```


### divmod(number, base)
---
* 함수 모양
  * divmod(a, b)
* 함수 설명
  * 두 숫자를 인자로 전달 받아 첫 번째 인자를 두번째 인자로 나눈 몫과 나머지를 tuple형식으로 반환함
  * 두 인자는 목소수가 아닌 숫자여야 함
* 예시 : 
  
```python 
# 10진수 -> n진수 변환 함수
def solution(n, base):
    answer = ''

    while n > 0:
        n, mod = divmod(n, base)
        answer += str(mod)
    return answer[::-1]
```

### <strong>collections.Counter 클래스</strong>
---
* collection 모듈의 클래스로 'from collections import Counter' 필수로 작성
* dictionary를 확장한 것으로, dictionary에서 제공하는 API그대로 사용 가능함
* 예제 
```python 
from collections import Counter

Counter('hello') 
# Counter({'l': 2, 'h': 1, 'e': 1, 'o': 1})

Counter('hello').most_common() # 데이터 개수가 많은 순으로 정렬
# [('l', 2), ('h', 1), ('e', 1), ('o', 1)]
```

