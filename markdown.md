### 1. Basic
***
#### 1-1. Header
-H1 ~ H6 까지 가능

```
큰   # H1
↓   ## H2
작  ### H3 
```
#### 1-2. 구분선 
`***` 입력 시 구분선이 생긴다.
#### 1-3. 글씨 폰트
-굵게 : `**글자**` => **글자**
-기울임 : `*글자*` => *글자*
#### 1-4. 목록
`* 항목` 입력시  결과
* 항목

***
### 2. link 삽입
***
```
방법 1
Click [링크이름](url)
Click [here](https://velog.io/)
```

결과👉 Click [here](https://velog.io/)
```
방법 2
벨로그 : https://velog.io/`
```
결과👉 벨로그 : https://velog.io/`
***

### 3. image 삽입
---
#### 3-1 기본 삽입


`![image description](이미지 상대경로 or 이미지 url)`

* 결과

<img src="https://images.velog.io/images/ena_hong/post/ca8530c0-eda1-4e86-959f-9aca06ef2df6/image.png" width=200>

***
#### 3-2 사이즈 조절
```
-이미지 태그<img>로 감싼 후 속성 width와 hight로 크기 조절
```

`<img src="이미지 상대경로 or url" width=150 hight=100>`

* 결과👇

<img src="https://images.velog.io/images/ena_hong/post/ca8530c0-eda1-4e86-959f-9aca06ef2df6/image.png" width=150>
***

#### 3-3 정렬 

**-가운데 정렬**
: 이미지 img태그를 p태그로 감싼다.

`<p align="center"><img src="image_src"></p>`
* 결과👇

<p align="center"><img src="https://images.velog.io/images/ena_hong/post/ca8530c0-eda1-4e86-959f-9aca06ef2df6/image.png" width=150></p>


**-왼쪽, 오른쪽 정렬**
: 왼쪽 정렬은 기본값이고 오른쪽 정렬은 이미지 태그에 align 속성을 준다.

`<img src="image_src" align="right">`
* 결과👉
<img src="https://images.velog.io/images/ena_hong/post/ca8530c0-eda1-4e86-959f-9aca06ef2df6/image.png" width=150 align="right">







***
### 4. 이모지 삽입
***

```
window : 윈도우 키 + 마침표(.)
mac: Command + Control + 스페이스 바
```
* 결과 : 😍🤩🌸🍁🌼
***
### 5. 글씨 색상
---
```
<span style="color:blue">쓰고싶은 내용</span>
<span style="color:red">red color</span>
<span style="color:green">**green color**</span>
```
* 결과 👇
* 
<span style="color:blue">쓰고싶은 내용</span>
<span style="color:red">red color</span>
<span style="color:green">**green color**</span>
***
### 6. Table 
---
```
`:` 세미콜론 이용하여 왼쪽, 오른쪽, 가운데 정렬 가능 

|Header|Description|Description|
|:--|:--:|--:|
|cell|cell|cell|
|cell|cell|cell|
```
* 결과 👇

|Header|Description|Description|
|:--|:--:|--:|
|cell|cell|cell|
|cell|cell|cell|
***
### 7. Code 
---
```
1.`(백틱) 사용하여 인라인 코드 작성

`print('Hello World')`
```
* 결과 👉 `print('Hello World')`
```
2. `(백틱) 위 아래로 ``` 3개 사용 하여 다수의 코드 작성

```　
import pandas as pd 
import seaborn as sns
```　
```
* 결과👇
```
import pandas as pd
import seaborn as sns
```
```
3. 해당 언어 표현 :```백틱 3개 뒤에 언어 넣는다 

```python
import random
a= int(random.random()*5)+1
print(a)
```　
```
* 결과👇
```python
import random
a= int(random.random()*5)+1
print(a)
```
***
### 8. Check Box 
---
`- [대괄호]`안에 띄어쓰기를 하면 빈 체크박스,`x`를 넣으면 체크된 체크박스가 생깁니다.
```
- [ ] 파이썬 공부하기
- [x] 판다스 공부하기
```
* 결과👇
- [ ] 파이썬 공부하기
- [x] 판다스 공부하기
***
>감사합니다. 
