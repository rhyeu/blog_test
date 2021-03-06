---
title: Today I Learn / python tip (print, list, 진법, 몫, 나머지)
author: 류성균
date: '2019-09-19'
slug: today-i-learn
categories:
  - Today I learn
tags:
  - python
---

<!--more-->

```{r}
library(reticulate)
Sys.setlocale('LC_ALL','C')
```

- 요새 코드업 기초 100제를 풀어보고 있는데 헷갈리는 것들을 정리!

# 1. sep 옵션 in python

파이썬에서 여러 개를 출력할 때 sep 옵션을 걸 수 있음

```{python}
print(1920, 1080, sep = 'x')
print('Hello', 'Python', sep = '-')
```

# 리스트 원소 합치기
- 출처 : http://mwultong.blogspot.com/2006/12/python-list-merge.html
```{python}
PA = ["pine", "apple"]

## 그냥 합치기
value = "".join(PA)
print(value)

## 구분자를 넣어 합치기
value2 = ", ".join(PA)
print(value2)
```


# 진법 변환
- 출처 : https://www.daleseo.com/python-int-bases/
```{python}
## 10진법 -> 다른 진법
format(50, 'b') # 이진법
format(50, 'o') # 8진법
format(50, 'x') # 16진법 (소문자)
format(50, 'X') # 16진법 (대문자)
format(50, 'X') # 16진법 (대문자)
```

```{python}
## 다른 진법 -> 10진법
format(int('2A', 16), 'd')
format(int('62', 8), 'd')
```

```{python}
### 다른 진법 -> 다른 진법
format(int('2A', 16), 'o')
format(int('62', 8), 'X')
```

# 항상 헷갈리는 몫과 나머지
- 참조 : https://programmers.co.kr/learn/courses/4008/lessons/12732
```{python}
a = 4; b = 7

print(a//b) # 몫
print(a%b) # 나머지
```

# 아스키 코드 <-> 문자열
```{python}
print(ord('B')) # 문자를 아스키 코드로 변환
print(chr(102)) # 아스키코드를 문자로 변환
```

# 리스트의 문자열을 int 형태로 변환
```{python}
a = ['13', '4', '68']

a1 = list(map(int, a)) # 맵핑을 이용한 방법
print(a1)
a2 = [int(i) for i in a] # 리스트 컴프리헨션을 이용한 방법
print(a2)
```
