# HTML, CSS, JS 기초


## HTML

> HTML : Hyper Text Markup Language
> 
> 웹페이지의 구조를 표시
> 
> 웹페이지의 컨텐츠를 표시
> 


### HTML Elements

> Element: 요소 - 의미식
> 
> Tag : 태그 - 기술적

> 문법(Syntax)
> 
> <>로 감싸줌
> 
> 소문자 사용
> 
> 시작태그와 종료태그 세트로 구성됨.
```
<tagname>contents</tagname>
```
> 
> 예외) 시작태그만 존재하는 경우 : 빈 요소(Empty Element)
>   - hr, br, img
> 
> 포함관계(Nested)
> 
```
<body>
  <div>
    text
  </div>
</body>
```


### HTML Attribute

> HTML 속성
> 
> HTML 요소의 부가 정보
> 
> 속성을 쓰는 문법 형태 : 속성이름 = "속성값"

```
<a href="http://www.naver.com">naver</a>
```


### HTML 페이지에서 표시하는 콘텐츠

- 텍스트 콘텐츠

- 멀티미디어 콘텐츠(임베디드(embeded) 콘텐츠)
  - 이미지
  - 비디오
  - 오디오


### 제목 태그

> heading -> h
> 
> h1~h6
> 
> h1이 가장 큰 제목


### HTML 기본 구조

```
<!DOCTYPE html> - 1
<html> - 2
  <head> - 3
    <meta charset="utf-8"> - 4
    <title>My test page</title> - 5
  </head>
  <body> - 6
    <p>This is my page</p>
  </body>
</html>
```

1. !DOCTYPE html ⇒ 웹 문서의 버전 : HTML5
2. html ⇒ HTML 문서의 가장 바깥쪽 요소
3. head ⇒ 웹 문서를 설명하는 정보가 담기는 영역 요소
4. meta charset="utf-8" ⇒ 웹 문서의 정보를 표시하는 요소
5. title ⇒ 웹 문서의 제목(브라우져의 타이틀에 표시)을 표시하는 요소
6. body ⇒ 웹 문서의 콘텐츠 요소들이 담기는 영역 요소


### 단락 태그
  
> p(Paragraph) : 단락을 표시
>
> 단락과 단락 사이를 구분하는 수평선
>
```
<hr> - Horizontal Rule
```
> 단락을 구분하지 않고 줄 바꿈
```
<br> - Break

```


### 목록 태그

> 순서 없는 목록 : ul(Unorderded List)
> 
> 순서 있는 목록 : ol(Ordered List)
>
> 목록 항목 : li(List Item)

```
<ul>
  <li>HTML</li>
  <li>CSS</li>
</ul>

<ol>
  <li>HTML</li>
  <li>CSS</li>
</ol>
```
> 포함관계(nested)로 구성된 목록 - 코딩할 대 밖에서 안쪽 방향 순서로 작성
- HTML
  - HTML4
  - HTML5
- CSS
  - CSS2
  - CSS3
```
<ul>
  <li>
    HTML
    <ul>
      <li>HHTML4</li>
      <li>HTML5</li>
    </ul>
  </li>
  <li>
    CSS
    <ul>
      <li>CSS2</li>
      <li>CSS3</li>
    </ul>
  </li>
</ul>
```

> 설명목록(Description List) = dl

```
<dl>
  <dt>HTML</dt>
  <dd>표준 마크업 언어</dd> (dd : Description Data)
</dl>
```


### HTML Hyper Link

> 하이터랑크 a(anchor)
>
> attribute(속성) : href(Hypertext Refrence) : 연결되는 웹 문서의 URL
```
<a href="http://www.nwver.com">네이버로 이동</a>
```
> 북마크 기능
> 
> 외부 페이지 연결이 아닌 같은 페이지엑서 특정위치로 이동할 수 있게 해주는 기능
> 
> 도착지점에 id attribute를 사용하여 이름을 지정
```
<a href="#t1"></a>
...
<h2 id="t1">제목<h2>
```


### Table Element 

> 기본 사용 태그 : table, thead, tbody, tr, th, td
> 
> 열 제목 : thead(table head), th(table heading)
> 
> 표 내용 : tbody(table body), td(table data)
> 
> 행 : tr(table row)

https://www.tablesgenerator.com/html_tables


### Image Element
> Tag : img
> 
> Attribute : src(image 위치, 파일명), alt(대체 텍스트)
```
<img src="image.jpg" alt="대체텍스트">
```

### Vidio Element

> 비디오 및 오디오 콘텐츠는 용량이 크기 때문에 서버에 저장을 해서 콘텐츠를 제공하면 많은 트래픽이 발생할 수 있음.
> 
> 트래픽 과부하를 해결하기 위해서 유튜브 서비스를 사용하기도 함.
> 
> attribute
> 
> controls : 컨트롤 버튼 표시
> 
> muted : 음소거
> 
> loop : 반복 재생


### Youtube

> 비디오 콘텐츠 제공시 서버의 트래픽 과부하를 해결할 수 있는 방법 중의 하나
> 
> 매개변수 ( src 주소의 쌍따옴표 안에 ?(물음표) 입력 후 매개변수 설정 / 매개변수를 여러개 설정시 공백 없이 &로 연결하여 입력 / 1은 설정, 0은 설정안함 )
> 
> - controls=1, 0
> 
> - autoplay=1, 0 (mute와 같이 사용 ⇒ ex. auotplay=1&mute=1)
> 
> - mute=1, 0
> 
> - loop=1, 0 (playlist와 같이 사용 ⇒ ex. loop=1&playlist=video_id)
>              
> - playlist=물음표앞의video_id
>
> 텍스트는 HTML 문서에 직접 입력되는 콘텐츠 ⇒ 텍스트(text) 콘텐츠
> 
> 이미지와 동영상, 오디오 콘텐츠는 외부에서 만들어지는 콘텐츠
> 
> 이미지, 동영상, 오디오는 직접 입력하는 것이 아니고 외부 파일을 삽입 ⇒ 임베드(embed) 콘텐츠


### 웹사이트 탬플릿 디자인(다운로드)
https://freebiesbug.com/psd-freebies/minimo-minimal-blog-template/


### Container Element(의미가 없는 단순 영역 구분 요소)
  : 영역의 의미가 애매한 경우 사용
> div(division)
> 
> span


### Block, Inline

> 모든 Element는 각각의 고유 영역을 가지고 있음
> 
> Block Element, INline Element 구분은 이들 영역의 화면 표시 방식에 따른 구분
> 
> * Block Element는 줄바꿈 되어 표시됨 - Block Element 영역의 가로 너비는 부모요소 너비의 100%로 채워짐
> (** 포함하는 요소 : 부모요소 / 포함되는 요소 : 자식요소)
> 
>     → Block Element에는 위, 아래 여백을 적용할 수 있음
> 
> * Inline Element는 같은 줄에 나란히 표시됨 - Inline Element 영역의 가로 너비가 콘텐츠 크기 만큼만 정해짐
> 
>     → Inline Element는 위, 아래 여백을 적용할 수 없음


### Parent Element(부모요소), Child Element(자식요소)

> 포함관계에서 포함하는 요소가 부모요소, 포함되는 요소가 
> 
> 직계 포함관계에서만 부모요소, 자식요소라고 함
> 
> 직계가 아닌 포함관계에서는 조상요소(Ancestor Element), 자손요소(descendant Element) 라고 함


### CSS 기본 개념
> 선택자는 스타일을 지정할 HTML 요소를 가리킵니다.
>
> 선언 블록에는 세미콜론으로 구분 된 하나 이상의 선언이 포함됩니다.
>
> 각 선언에는 콜론으로 구분된 CSS 속성(Property)이름과 값(Value)이 포함됩니다.
>
> 여러 CSS 선언은 세미콜론으로 구분하고 선언 블록은 중괄호로 묶습니다.


### id, class

> HTML Element에 특정 이름을 사용할 때 id, class attribute를 사용해서 이름을 붙여줄 수 있음.
> 
> id는 동일한 이름이 사용된 HTML Element가 여러개이면 논리적 오류가 발생
> 
> id는 HTML문서 내에서 고유해야 함
> 
> class는 동일한 이름이 여러개의 Element에 사용되어서 공통 디자인 요소나 공통 기능을 적용할 수 있음.
> 
> id는 주로 서버에서 불러오는 데이터를 표시하는 위치에 고유하게 사용 => 백엔드 개발에서 주로 사용
> 
> class는 주로 css 스타일 적용, javascript 인터랙션을 적용할 때 사용 => 프론트엔드 개발에서 주로 사용
> 
> id는 하나의 HTML Element에 대해서 하나의 이름만 존재해야하며, HTML문서 내에서도 고유해야 함.
> 
> class는 하나의 HTML Element에 대해서 여러개의 이름을 지정할 수 잇고, HTML문서 내에서 여러 곳에서 공통 사용이 가능함.


### CSS 작성방법

> External CSS : 파일 분리
> 
> Internal CSS : 같은 HTML문서 내에 head 태그 영역에  style 태그를 사용하여 입력 
>
> Inline CSS : 시작태그에 style attribute를 사용해서 입력 => javascript에서 css를 제어할 때 사용


### naming할 때 표기방식

> id/class naming, 변수/함수 naming, 파일/폴더 naming의 경우 가독성을 높이기 위해 사용
> 
> 표기방식을 사용하는 이유 : naming할 때 두 단어 이상으로 구성되는 경우 단어 사이를 구분하기 위해
> 
>   ⇒ 단어 시작부분의 첫글자를 대문자로 변경하거나 특수기호를 사용
> 
> 표기방식 종류
> 
> * snake case : 파일/폴더 이름에 사용  ⇒ ex) gnb_depth1
> 
> * kebab case : id/class 이름에 사용  ⇒ ex) gnb-depth1
>
> * camel case : javascript의 변수/함수 이름에 사용  ⇒ ex) gnbDepth1
> 
> * Pascal case : javascript의 클래스 이름에 사용  ⇒ ex) GnbDepth1



### OOCSS(Object Oriented CSS)

> HTML Element를 대상화시키는 과정에서 Element 하나하나를 모두 객체화 시키는 이론
> 
> HTML Element 모두 각각 id, class attribute를 사용해서 이름을 지정해줌.


### Web Color
> color mode
> 
> - 가산혼합(빛의혼합) : RGB 컬러모드

> 표현할 수 있는 색의 수
> 
> 1byte = 8bit = 256개 (0~255)
> 
> RGB => 3byte => 24bit 트루컬러 : 16,777,216가지 색

> 색 표현 코드값
> 
> - 16진수(hex code) : #AABA01  (16진수의 코드값이라는 것을 표현하기 위해 코드 앞에 #을 붙여준다.)
> 
> - 10진수 : 255, 255, 255

> CSS 사용법

```
color : #34ebae
color : rgb(52, 235, 174);
color : rgba(52, 235, 174, 0.5);
```

> 투명도를 표현하는 용어
> 
> - transparent : 투명한
> 
> - alpha : 투명도 설정 ⇒ RGB(8비트 크기의 채널 3개) 이외에 추가되는 8비트 크기의 채널 
> 
> - opacity : 불투명도 설정


### Text CSS
- color
- text-align : lefr, center, right, justify  --> 정렬
- text-decoration : underline, line-through, overline, none  --> 텍스트 라인
- text-transform : uppercase, lowercase, Capitalize
- text-indent : 20px / -20px  ( 들여쓰기는 양수, 내어쓰기는 음수로 입력)
- letter-spacing : 2px / -2px  --> 띄어쓰기 
- line-height : 20px / 1.8(배수)  --> 줄간격
- word-spacing
- white-space : nowrap ( nowrap --> 화면 너비보다 텍스트의 길이가 길어도 줄바꿈을 안하고 한줄로 나오게 설정하여 가로 스크롤바 생김)
- text-shadow  --> 그림자


### Font CSS
- font-family : "Times New Roman", Times, serif;
  - 순서대로 대체 폰트를 찾음
  - sans-serif, serif, monospace, cursive, fantasy 5개의 기본폰트는 font-family 사용시 종류에 맞게 항상 끝에 기본으로 사용됨
  - 웹사이트에 사용하는 폰트는 웹폰트(서버에 폰트파일을 저장해서 사용)로 사용하는데, 업로드된 파일을 직접 사용하는 경우, 웹폰트 서비스를 사용하는 경우 2가지가 있음
  - 대표적인 웹폰트 서비스 : 구글 폰트(https://fonts.google.com), 눈누(https://noonnu.cc)
- font-soze
- font-style : italic
- font-weight : bold / 500
  - 폰트 굴기가 다양한 경우 숫자로 굵기를 표현


### Box Model
> 구성요소
>
> - width / height : 너비/높이
> 
> - padding : 안쪽 여백
> 
> - border : 테두리
> 
> - margin : 바깥 여백


### width/height
> width : 너비/가로길이
> 
> height : 높이/세로길이
>
> auto : 기본값
> 
> - Block : 너비 : 부모요소를 기준으로 채워짐 / 높이 : 콘텐츠(자식요소)를 기준으로 채워짐
> 
> - Inline : 너비/높이 : 콘텐츠(자식요소)에 맞춰짐


### Padding
> 안쪽여백

> padding-top
>
> padding-right
> 
> padding-bottom
> 
> padding-left

> padding : 10px 20px 30px 40px (top right bottom left)
> 
> padding : 10px 20px 30px (top right/left bottom)
> 
> padding : 10px 20px (top/bottom right/left)
> 
> padding : 10px (top/right/bottom/left)


### margin
> Padding과 사용방법이 같음

> margin collapse
> 
> - 위,아래 인접하게 배치된 박스의 사이 여백이 둘 중 큰쪽으로만 적용되어 표현되는 현상
>
> - 위,아래 양족으로 margin을 적용하는 것보다 한쪽을 기준으로 적용하는 것이 더 효율적임


### Border
> border : 1px solid red; ( ⇒ 4방향 모두 적용 )
> 
> border-top : 1px solid red; ( ⇒ top만 적용 )
> 
> border-right : 1px solid red; ( ⇒ right만 적용 )
> 
> border-bottom : 1px solid red; ( ⇒ bottom만 적용 )
> 
> bordr-left : 1px solid red; ( ⇒ left만 적용 )


### 가로 배치

※ Inline 요소는 박스 모델이 제대로 적용되지 않으므로 레이아웃 구성요소로 사용하기 어렵기 때문에 Block 요소를 레이아웃 구성요소로 사용함 ⇒ 세로 배치는 기본 구성

가로 배치 기법
- float
- flex
- grid


### Float
> left, right 값을 사용해서 가로 배치
> 
> left, right는 부모요소를 기준으로 방향성을 표현
> 
> 일반적으로 왼쪽을 기준으로 순서대로 배치할 때 left만 사용해서 배치

> float은 박스가 띄워지는 현상이 있기 때문에 인접새 있는 박스의 배치가 깨질 수 있음
> 
> float 박스를 부모요소로 감싸서 인접해 있는 박스와 float 박스를 감싸고 있는 부모요소와의 관계로 만들어줌
> 
> float 박스를 감싸는 부모요소는 높이가 0이 될 수 있기 때문에 그것을 clear할 수 있는 비어있는 자식요소를 넣어줌
```
HTML
<div class="float-container">
  <div class+"float-box">test</div>
  <div class="float-box">test</div>
  <div class="clearfix"></div>
</div>

CSS
.float-box {
  float:left;
}
.clesrfix {
  clear:both;
}
```


### Display 속성
> 요소의 기본 속성을 변형하지 않고 화면에 표시되는 속성을 변형
> 
> block, inline, inline-block

```
div {
  display:inline;
}
⇒ div : inline 속성으로 화면에 표시

> inline-block : inline의 속성(한줄에 나란히 표시되는 속성)과 block의 속성(박스모델이 적용되는 속성)을 모두 표시
```

### Form 요소
> 웹페이지에서 사용자 입력을 받아 사용하는 요소

```
<input type="test"> : 일반 텍스트를 입력하는 경우
<input type="password"> : 비밀번호를 입력하는 경우

<input type="button" value="확인"> : 시작 태그만 있고 종료 태그가 없어서 value 속성으로 텍스트를 입력해야 함
<button type="button">확인</botton> : 
```


### 이미지 표현 방법
> 콘텐트로 표현
> - img 태그
> 
> 디자인 요소로 표현(content의 의미와는 상관없는 배경이미지)
> - background-image

> IR(Image Replacement : 이미지로 대체) 기법
> - HTML Element에는 텍스트로 표시
> - 화면(브라우져)에 표시할 때는 이미지로 표현

### Background
> background-color
> 
> background-image
> 
> background-repeat
> 
> - repeat-x (가로만 반복)  /  repeat-y (세로만 반복)  /  no-repeat (반복없음)
> 
> background-pasition
> 
> background-position
>
> - left, center, right / top, center, bottom : 키워드
> 
> - px 좌표 표시
```
div{
  background-position:left top;(앞:가로방향/뒤:세로방향)
  background-position:100px 200px;(앞:가로방향/뒤:세로방향)
}
```
> background-attachment
>  - 배경이미지를 고정

> background 축약표현
```
background:#fff;
background:url("image.jpg")
```


### 반응형 웹

> OSMU(One Source Multi Use)
> - One Source : HTML
> - Multi Use: CSS, Javascript

> 변경점(break point)
> - 기준 해상도를 설정하고 범위 구간으로 설정

> @media
```
@media 디바이스 and (구간 해상도){
  디바이스 스타일
}

@media screen and (max-width:300px){}  // 최대 가로길이 지정하는 경우
@media screen and (min-width:300px){}  // 최소 가로길이 지정하는 경우

// 독립된 구간으로 설정하는 경우 --> 동일한 속성도 각각 따로 설정해줘야 하는 단점이 있음 (코드가 길어짐)
@media screen and (min-width:360px) and (max-width:700px){
  /* 스마트폰 CSS  */
} 
@media screen and (min-width:701px) and (max-width:1920px){
  /* PC CSS  */
}

// 포함된 구간으로 설정하는 경우 --> 동일한 속성은 한번만 입력해도 되기 때문에 코드가 짧아짐 (두 영역의 속성을 비교하며 코딩을 해야하는 번거러움이 있음)
    : 스마트폰 구간이 PC 구간 안에 포함되며, PC 구간이 오픈된 범위로 사용됨
/* PC CSS  */
@media screen and (max-width:700px){
  /* 스마트폰 CSS  */
}
  
@mesia screen an

```


### JavaScript


### DOM


### Event
> 상황 변화에 따라 발생되는 신호

> Event 발생
> - Event 감지 : 종류, 상황
> - 감지한 Event에 맞는 기능, 동작 실행

> Event 종류
> - Mouse Event: click, mouse over, mouse out
> - Keyboard Event : Key 입력

> Event 감지 함수
> - javascript : addEventListener()
> - jquery: on()

함수 : 익명함수 정리
