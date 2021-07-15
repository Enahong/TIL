## [주피터 노트북]
* 로컬 아나콘다 주피터 노트북 상에서의 설정
### Matplotlib을 통한 설정
[matplotlib.pyplot.rc — Matplotlib 3.1.3 documentation](https://matplotlib.org/3.1.3/api/_as_gen/matplotlib.pyplot.rc.html)

#### 1. 시각화 스타일 설정
* 일부 스타일은 폰트설정을 초기화하기 때문에 style 설정 시 폰트 설정이 초기화 되지 않도록 폰트 설정 위에서 지정해 줄것
```python
# 템블릿 
print(plt.style.available)
>>>['Solarize_Light2', '_classic_test_patch', 'bmh', 'classic', 
'dark_background', 'fast', 'fivethirtyeight', 'ggplot', 'grayscale', 
'seaborn', 'seaborn-bright', 'seaborn-colorblind', 'seaborn-dark', 
'seaborn-dark-palette', 'seaborn-darkgrid', 'seaborn-deep', 
'seaborn-muted', 'seaborn-notebook', 'seaborn-paper', 'seaborn-pastel', 
'seaborn-poster', 'seaborn-talk', 'seaborn-ticks', 'seaborn-white', 
'seaborn-whitegrid', 'tableau-colorblind10']
```
```python
plt.style.use('fivethirtyeight')
```
#### 2. 폰트 설정
* 아래 코드로 한글 폰트와 마이너스 값이 깨짐없이 정상 출력되도록 한다
```python
# 윈도우에서 한글폰트가 깨지지 않게 하기 위한 설정
# '-' 값이 깨지지 않게 하기 위한 설정 
plt.rc("font", family= "Malgun Gothic") 
plt.rc("axes", unicode_minus = False)  # '-' 값이 깨지지 
```
#### 3. 시각화 선명하게 설정
* retina 디스플레이가 지원되는 환경에서 시각화의 폰트가 좀 더 선명해 보입니다.
```python
    from IPython.display import set_matplotlib_formats
    set_matplotlib_formats('retina')
```

#### 4. 잘 설정이 되었는지 확인
```python
pd.Series([1,3,5,-7,9]).plot(title='한글')
```
<img src="https://images.velog.io/images/ena_hong/post/fab231e5-9773-4d46-a52e-e50484891c9c/image.png" width=400>

***
### Seaborn을 통한 설정

#### 1. 스타일. 폰트 설정 
```python
# style = {darkgrid, whitegrid, dark, white, ticks}

sns.set_theme(font ='Malgun Gothic',
        	rc = {'axes.unicode_minus' : False},
        	style ='whitegrid')
```
#### 2. 시각화 선명하게 하기
```python
    from IPython.display import set_matplotlib_formats
    set_matplotlib_formats('retina')
```
#### 3. 잘 설정되었는지 확인
```python
pd.Series([1,3,5,-7,9]).plot(title= '한글')
```
<img src='https://images.velog.io/images/ena_hong/post/cc30f007-0803-4f58-ac98-0784a530497b/image.png' width=400>

***
## [Google Colab]
* google colaboratory 에서의 설정 
#### 1. 폰트 설정하기
```python
# 나눔고딕 설치
#!apt -qq -y install fonts-nanum > /dev/null

import matplotlib.font_manager as fm
fontpath = '/usr/share/fonts/truetype/nanum/NanumBarunGothic.ttf'
font = fm.FontProperties(fname=fontpath, size=9)
fm._rebuild()

 plt.rc('font', family='NanumBarunGothic') 
 ```
 #### 2. 시각화 선명하게 설정하기
 ```python
 %config InlineBackend.figure_format = 'retina'
 ```
