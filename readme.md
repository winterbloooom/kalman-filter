# What is in this Repository?
해당 내용은 책 <칼만 필터는 어렵지 않아 with MATLAB Examples(김성필, 한빛아카데미)>를 참고하였습니다. 

본 책에서는 MATLAB을 사용해 각종 필터를 구현하나, 해당 레포지토리에서는 Python을 사용하였으며, `matplotlib.pyplot` 등의 라이브러리를 활용해 데이터를 시각화하였습니다.

# Dataset
## Download
실습에 사용한 일부 데이터들은 책에서 제공하고 있는 것을 사용했습니다. 자료는 [출판사 자료실](https://www.hanbit.co.kr/store/books/look.php?p_code=B4956047798)에서 다운받을 수 있습니다.

## Usage
출판사에서 제공되고 있는 파일은 MATLAB 자료, 즉 `*.mat` 파일이므로 이를 Python에서 이용하기 위한 약간의 변환 과정이 필요합니다.

`scipy.io` 라이브러리를 이용해 파일을 읽어들일 수 있으며, 딕셔너리 형태로 가져온 파일 내용 중 원하는 것을 사용합니다.

```py
from scipy import io
```
```py
mat_file = io.loadmat('./SonarAlt.mat')
	# mat 파일의 경로를 입력해준다.

print(mat_file)
	# mat 파일의 내용을 살펴본다.
	# {'__header__': b'MATLAB 5.0 MAT-file, Platform: PCWIN, Created on: Thu Feb 25 13:19:03 2010', 
    # '__version__': '1.0', 
    # '__globals__': [], 
    # 'sonarAlt': array([[34.25491256, 33.60223519, 33.60223519, ..., 36.55540305, 36.55540305, 36.55540305]])}

print(mat_file['sonarAlt'])
    # [[34.25491256 33.60223519 33.60223519 ... 36.55540305 36.55540305 36.55540305]]
```

# Blog Posting
[저의 블로그](https://velog.io/@717lumos)에 해당 내용을 포스팅하고 있습니다. 이론을 위주로 볼 때는 이곳이 보기 더 편할 것 같습니다. 😎
