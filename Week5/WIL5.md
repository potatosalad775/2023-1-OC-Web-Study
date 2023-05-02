# WIL5

## HTML5

HTML은 웹페이지를 기술하기 위한 마크업 언어로, 웹페이지의 내용과 구조를 담는다.

## Using HTML5

* HTML5 문서는 반드시 `<!DOCTYPE html>`로 시작하여 문서 형식을 HTML5로 지정해야 한다.
* 실질적인 HTML Document 내용은 `<html>`과 `</html>` 태그 사이에 기술된다.
* `<head>`와 `</head>` 사이에는 문서 제목, 외부 파일 참고, 메타데이터 설정 등 브라우저에 표시되지 않는 정보들이 담겨진다.
* 웹브라우저에 출력되는 모든 요소는 `<body>`와 `</body>` 사이에 위치한다.

## HTML5의 기본 문법

### 요소

HTML의 요소는 시작 태그, 종료 태그, 그리고 두 태그 사이에 위치한 content로 구성된다.

HTML Document는 이렇게 구성된 요소들의 집합으로 이루어진다.

요소는 중첩될 수 있다. 이 때 부자관계가 성립되는 것으로 본다. 이 중첩 관계를 통해 웹페이지의 구조를 표현한다.

* 빈 요소 (Empty Element) : content를 가질 수 없는 요소를 빈 요소라고 한다. 이 때 어트리뷰트(Attribute) 만을 가질 수 있다.

### 어트리뷰트 (Attribute)

어트리뷰트는 요소의 성질, 특징을 정의하는 명세이다. 요소는 어트리뷰트를 가질 수 있으며, 요소에 추가적인 정보를 제공한다. 어트리뷰트는 시작 태그에 위치하며, 이름과 값의 쌍을 이룬다.

```HTML
<img src="html.png">
// src = 어트리뷰트 이름
// "html.png" = 어트리뷰트 값
```

* 글로벌 어트리뷰트 
 
모든 HTML 요소가 공통으로 사용할 수 있는 어트리뷰트. 

id, class, style, title 등이 있다.

### 주석 (Comment)

```HTML
<!--주석은 화면에 표시되지 않는다.-->
<p>Lorem ipsum dolor sit amet</p>
```

## Sementic Web

웹사이트는 검색엔진에서의 노출이 매우 중요하다.

검색 엔진은 로봇이라는 프로그램을 사용해 매일 **전세계의 웹사이트 정보를 수집**하는데, 이를 **크롤링**이라고 한다. 

이 과정에서 사용자가 검색할만한 **키워드를 미리 예상**하여 인덱스를 만들어둔다. 이를 **인덱싱**이라 한다.

인덱스를 생성할 때 사용되는 정보는 검색 로봇이 수집한 정보인데, 이는 결국 웹사이트의 HTML 코드이다. 이 과정에서 **시맨틱 요소를 해석**하게 된다.

**시맨틱 태그**는 브라우저, 검색엔진, 개발자 모두에게 **콘텐츠의 의미를 명확히 설명**하는 역할을 한다. 

개발자가 의도한 요소의 의미를 정확하게 전달하여 코드의 가독성을 높이고 유지보수를 쉽게하는 것과 동시에, 검색엔진의 효과적인 크롤링과 인덱싱을 가능하게 한다.

**시멘틱 웹**이란 웹에 존재하는 수많은 웹페이지들에 메타데이터를 부여하여, 기존의 잡다한 데이터 집합이었던 웹페이지를 '의미'와 '관련성'을 가지는 거대한 데이터베이스로 구축하고자 하는 발상이다.

HTML 요소는 non-semantic 요소, semantic 요소로 나눌 수 있다.

* non-semantic 요소 : content에 대해 어떠한 설명도 하지 않는 태그 - div, span 등
* semantic 요소 : content의 의미를 명확히 설명하는 태그 - form, table, img 등

## HTML 기본 태그

### 문서 형식 정의 태그

출력할 웹페이지의 형식을 브라우저에 전달한다. 문서의 최상단에 위치해야하며 대소문자를 구별하지 않는다.

```HTML
<!DOCTYPE html>
```

### html 태그

모든 HTML 요소의 부모 요소이며, 웹페이지에 단 하나만 존재한다. 모든 요소는 html 요소의 자식 요소이며, html 요소 안에 기술된다. 단, `<!DOCTYPE>`은 예외이다.

### head 태그

메타데이터를 담기 위한 요소로, 웹페이지에 하나만 존재한다. 문서의 title, style 등에 대한 데이터를 담고, 화면에 표시되지 않는다.

* title : 문서의 제목을 정의한다. 브라우저 탭 등에 표시된다.
* style : HTML 문서를 위한 style 정보를 정의한다.
* link : 외부 리소스와의 연계 정보를 정의한다.
* script : client-side JavaScript를 정의한다.
* meta : 기타 메타데이터 정의에 사용된다. 특히, charset 어트리뷰트는 브라우저가 사용할 문자셋을 정의한다.

```HTML
<!--SEO(검색엔진 최적화)를 위해 검색엔진이 사용할 keywords을 정의한다.-->
<meta name="keywords" content="HTML, CSS, XML, XHTML, JavaScript">

<!--웹페이지의 설명을 정의한다.-->
<meta name="description" content="Web tutorials on HTML and CSS">

<!--웹페이지의 저자을 명기한다.-->
<meta name="author" content="John Doe">

<!--웹페이지를 30초 마다 Refresh한다.-->
<meta http-equiv="refresh" content="30">
```

### body 태그

HTML 문서의 내용을 나타내고, 웹페이지에 하나만 존재한다. 웹페이지를 구성하는 대부분의 요소가 body 요소 내에 기술된다.

## Text 관련 태그

### 제목 태그

Heading 태그는 제목을 나타낼 때 사용하며, h1 ~ h6까지의 태그가 있다.

시맨틱 웹의 의미를 살려서, 제목 이외에는 사용하지 않는 것이 좋다.

### 글자 형식 태그

* b : 볼드체, 다만 의미론적(Semantic) 중요성 없음.
* strong : 볼드체, 그러나 의미론적 중요성을 가짐. 웹표준을 준수하고자 한다면 strong을 사용하는 것이 바람직하다.
* i : Italic체. 의미론적 중요성 없음.
* em : Emphasized (강조된) 텍스트 표현. 이탤릭체로 표현되나, 의미론적 중요성을 가진다.
* small : 작은 텍스트 표현
* mark : 형광펜처럼 하이라이트된 텍스트 표현
* del : 취소선이 그어진 텍스트 표현
* ins : 삽입된 텍스트 표현. 언더바가 삽입된다.
* sub / sup : 아래 / 위 첨자 표현

### 본문 태그

* p : Paragraph. 단락 지정
* br : 강제 개행 지정. - 연속 공백 삽입 시 `&nbsp;`를 사용한다.
* pre : 형식화된 텍스트 지정.
* hr : 수평줄 삽입
* q : 짧은 인용문 지정
* blockquote : 긴 인용문 지정
  
## CSS

CSS는 HTML과 같은 문저를 어떻게 렌더링할 지 정의하기 위한 언어이다. 각 요소의 style을 정의하여 설명하기 위해 작동한다.

HTML5에서 HTML은 정보와 구조화, CSS는 Styling의 정의라는 확실한 구분이 생겼다.

### Selector

CSS는 HTML 요소의 Style을 정의하는데 사용된다. 이를 위해 스타일을 적용하고자 하는 HTML 요소를 선택할 수 있어야한다.

셀렉터는 HTML 요소를 선택하기 위해 CSS에서 제공하는 수단이다.

```CSS
h1 { color: red; font-size: 12px; }
```

위 구문을 Rule Set이라고 하며, HTML 문서 속 셀렉터를 통해 모든 h1 요소를 선택한 후 선택된 h1 요소의 스타일을 중괄호로 표현된 선언 블록 안에서 여러 선언들로 정의하고 있다.

이와 같은 Rule Set의 집합을 스타일 시트라고 한다.

### Property (속성) + Value (값)

셀렉터로 HTML 요소를 선택하고 {} 내에 프로퍼티(속성)과 값을 지정하는 것으로 다양한 스타일을 지정할 수 있다. 표준 스펙으로 이미 지정되어 있는 것을 사용해야 하며 여러 프로퍼티들은 세미콜론으로 구분한다. 각 프로퍼티에 할당되는 값은 특정 단위로 지정해야 한다. 이러한 단위에는 px, % 등이 존재한다.

```CSS
p {
    color: red;
    font-size: 12px;
}
```

### HTML과 CSS의 연동

#### 1. Link Style

HTML에서 외부에 있는 CSS를 불러오는 방식이다.

```HTML
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" href="css/style.css">
  </head>
  <body>
    <h1>Hello World</h1>
    <p>This is a web page.</p>
  </body>
</html>
```

```CSS
h1 { color: red; }
p  { background: blue; }
```

#### 2. Embedding Style

HTML 내부에 CSS를 포함시키는 방식이다. 간단한 웹이라면 문제는 없겠지만 Link Style이 보다 권장된다. 서로 역할이 다르기 때문이다.

```HTML
<!DOCTYPE html>
<html>
  <head>
    <style>
      h1 { color: red; }
      p  { background: aqua; }
    </style>
  </head>
  <body>
    <h1>Hello World</h1>
    <p>This is a web page.</p>
  </body>
</html>
```

#### 3. Inline Style

HTML 요소의 Style 프로퍼티 안에 CSS를 기술하는 방식. JavaScript가 동적으로 CSS를 생성할 때 사용하는 경우가 있으나, 마찬가지로 Link Style이 보다 권장된다.

```HTML
<!DOCTYPE html>
<html>
  <body>
    <h1 style="color: red">Hello World</h1>
    <p style="background: aqua">This is a web page.</p>
  </body>
</html>
```

### Reset CSS 사용하기

모든 웹브라우저는 자체적인 기본 스타일이 있으나, 브라우저마다 제각각이므로 주의가 필요하다.

Reset CSS는 기본적인 HTML 요소의 CSS를 초기화하는 목적으로 사용한다. 즉, 브라우저 별로 제각각인 기본 스타일을 하나의 스타일로 통일시켜주는 역할을 한다.

자주 사용되는 Reset CSS는 다음과 같다.

* Eric Meyer's reset
* normalize.css

## CSS - Selector

셀렉터는 복수개를 연속하여 지정이 가능하다.

```CSS
h1, p { color: red; }
```

### Universal Selector

\* : HTML 문서 내 모든 요소를 선택한다. HTML 요소를 포함하며, head 요소도 포함된다.

```HTML
<style>
    * { color: red; }
</style>
```

### Tag Selector

태그명 : 지정된 태그명을 가진 요소를 선택한다.

```HTML
<!DOCTYPE html>
<html>
<head>
  <style>
    /* 모든 p 태그 요소를 선택 */
    p { color: red; }
  </style>
</head>
<body>
  <p>paragraph</p>
</body>
</html>
```

### ID Selector

#id 어트리뷰트 값 : id 어트리뷰트 값을 지정하여 일치하는 요소를 선택한다. id 어트리뷰트 값은 중복될 수 없는 유일한 값이다.

```HTML
<!DOCTYPE html>
<html>
<head>
  <style>
    #p1 { color: red; }
  </style>
</head>
<body>
  <div class="container">
    <p id="p1">paragraph 1</p>
    <p id="p2">paragraph 2</p>
  </div>
  <p>paragraph 3</p>
</body>
</html>
```

### Class Selector

.class 어트리뷰트 값 : class 어트리뷰트 값을 지정하여 일치하는 요소를 선택한다. class 어트리뷰트 값은 중복될 수 있다.

```HTML
<!DOCTYPE html>
<html>
<head>
  <style>
    .container { color: red; }
  </style>
</head>
<body>
  <h1>Heading</h1>
  <div class="container">
    <p id="p1">paragraph 1</p>
    <p id="p2">paragraph 2</p>
  </div>
  <p>paragraph 3</p>
</body>
</html>
```

HTML 요소 내 클래스 어트리뷰트 값은 공백으로 구분하여 여러 개 지정이 가능하다. 미리 스타일을 정의해두고, HTML에서 이미 정의된 클래스를 지정하는 것으로 스타일을 지정할 수 있다. 이는 재사용의 측면에서 유용하다.

```HTML
<!DOCTYPE html>
<html>
<head>
  <style>
    .text-center { text-align: center; }
    .text-large  { font-size: 200%; }
    .text-red    { color: red; }
    .text-blue   { color: blue; }
  </style>
</head>
<body>
  <p class="text-center">Center</p>
  <p class="text-large text-red">Large Red</p>
  <p class="text-center text-large text-blue">Center Large Blue</p>
</body>
</html>
```

### Attribute Selector

* 셀렉터[어트리뷰트] : 지정된 어트리뷰트를 갖는 모든 요소를 선택한다.
* 셀렉터[어트리뷰트=”값”] : 지정된 어트리뷰트를 가지며 지정된 값과 어트리뷰트의 값이 일치하는 모든 요소를 선택한다.
* 셀렉터[어트리뷰트~=”값”] : 지정된 어트리뷰트의 값이 지정된 값을 (공백으로 분리된) 단어로 포함하는 요소를 선택한다.
* 셀렉터[어트리뷰트|=”값”] : 지정된 어트리뷰트의 값과 일치하거나 지정 어트리뷰트 값 뒤 연이은 하이픈(“값-“)으로 시작하는 요소를 선택한다.

이 외에도 다양한 선택 방법이 존재한다.

```HTML
<!DOCTYPE html>
<html>
<head>
  <style>
    a[href] { color: red; }
    a[target="_blank"] { color: blue; }
    h1[title~="first"] { color: yellow; }
    p[lang|="en"] { color: red; }
  </style>
</head>
<body>
  <h1 title="heading first">Heading first</h1>
  <a href="http://www.poiemaweb.com">poiemaweb.com</a><br>
  <a href="http://www.google.com" target="_blank">google.com</a><br>
  <a href="http://www.naver.com" target="_top">naver.com</a>
  <p lang="en">Hello!</p>
  <p lang="en-gb">Ello!</p>
</body>
</html>
```

이 외에도 다양한 셀렉터가 존재한다.

## 박스 모델

모든 HTML 요소는 Margin - Border - Padding - Content로 구성된 박스 형태의 영역을 가지고 있다.

브라우저는 박스 모델의 크기와 프로퍼티를 기반으로 렌더링을 수행한다.

* Content : 요소의 텍스트나 이미지 등의 실제 내용이 위치하는 영역이다. width, height 프로퍼티를 갖는다.
* Padding : 테두리(Border) 안쪽에 위치하는 요소의 내부 여백 영역이다. padding 프로퍼티 값은 패딩 영역의 두께를 의미하며 기본색은 투명(transparent)이다. 요소에 적용된 배경의 컬러, 이미지는 패딩 영역까지 적용된다.
* Border : 테두리 영역으로 border 프로퍼티 값은 테두리의 두께를 의미한다.
* Margin : 테두리(Border) 바깥에 위치하는 요소의 외부 여백 영역이다. margin 프로퍼티 값은 마진 영역의 두께를 의미한다. 기본적으로 투명(transparent)하며 배경색을 지정할 수 없다.

박스 모델에 적용되는 프로퍼티에는 box-sizing, border, margin/padding 등 다양하다.

## 폰트와 텍스트

폰트 및 텍스트 관련 프로퍼티는 폰트의 크기, 스타일, 텍스트 정렬 등을 정의한다.

* font-size : 텍스트 크기 정의
* font-family : 폰트 지정, 컴퓨터에 설치되지 않은 폰트의 경우 적용되지 않음. 여러 개 지정 시 다음에 지정된 폰트를 적용한다.
* font-style : 이탤릭체 지정
* font-weight : 폰트 굵기 지정
* line-height : 텍스트 높이 지정. 텍스트 수직 정렬에도 응용되어 사용된다.
* letter-spacing : 글자 사이 간격 지정.
* text-align : 텍스트 수평 정렬 정의.
* white-space : 공백, 들여쓰기, 줄바꿈 동작 제어.
* text-overflow : 부모를 벗어난, 자동 줄바꿈이 되지 않은 텍스트 처리 방법 정의.
* word-wrap / word-break : 단어가 너무 길어 부모 영역을 벗어난 텍스트 처리 방법 정의.

Shorthand Syntax도 제공된다.

```
font : font-style(optional) font-variant(optional) font-weight(optional) font-size(mandatory) line-height(optional) font-family(mandatory)
```

## Position 프로퍼티

### Static

Position 프로퍼티의 기본값. 

기본적인 요소의 배치 순서에 따라 위에서 아래로, 왼쪽에서 오른쪽으로 순서에 따라 배치되며 부모 요소 내에 자식 요소로서 존재할 때는 부모 요소의 위치를 기준으로 배치된다.

### Relative

기본 위치(static으로 지정되었을 때의 위치)를 기준으로 좌표 프로퍼티(top, bottom, left, right)를 사용하여 위치를 이동시킨다. static을 선언한 요소와 relative를 선언한 요소의 차이점은 좌표 프로퍼티의 동작 여부뿐이며 그외는 동일하게 동작한다.

### Absolute

부모 요소 또는 가장 가까이 있는 조상 요소(static 제외)를 기준으로 좌표 프로퍼티(top, bottom, left, right)만큼 이동한다. 즉, relative, absolute, fixed 프로퍼티가 선언되어 있는 부모 또는 조상 요소를 기준으로 위치가 결정된다.

만일 부모 또는 조상 요소가 static인 경우, document body를 기준으로 하여 좌표 프로퍼티대로 위치하게 된다.

따라서 부모 요소를 배치의 기준으로 삼기 위해서는 부모 요소에 relative를 정의하여야 한다.

이때 다른 요소가 먼저 위치를 점유하고 있어도 뒤로 밀리지 않고 덮어쓰게 된다. (이런 특성을 부유 또는 부유 객체라 한다)

absolute 선언 시, block 레벨 요소의 width는 inline 요소와 같이 content에 맞게 변화되므로 적절한 width를 지정하여야 한다.

relative 프로퍼티와 absolute 프로퍼티의 차이점은 아래와 같다.

relative 프로퍼티는 기본 위치(static으로 지정되었을 때의 위치)를 기준으로 좌표 프로퍼티(top, bottom, left, right)을 사용하여 위치를 이동시킨다. 따라서 무조건 부모를 기준으로 위치하게 된다.

absolute 프로퍼티는 부모에 static 이외의 position 프로퍼티가 지정되어 있을 경우에만 부모를 기준으로 위치하게 된다. 만일 부모, 조상이 모두 static 프로퍼티인 경우, document body를 기준으로 위치하게 된다.

따라서 absolute 프로퍼티 요소는 부모 요소의 영역을 벗어나 자유롭게 어디든지 위치할 수 있다.

### Fixed

부모 요소와 관계없이 브라우저의 viewport를 기준으로 좌표프로퍼티(top, bottom, left, right)을 사용하여 위치를 이동시킨다.

스크롤이 되더라도 화면에서 사라지지 않고 항상 같은 곳에 위치한다.

fixed 프로퍼티 선언 시, block 요소의 width는 inline 요소와 같이 content에 맞게 변화되므로 적절한 width를 지정하여야 한다.

## z-index 프로퍼티

z-index 프로퍼티에 큰 숫자값을 지정할수록 화면 전면에 출력된다. positon 프로퍼티가 static 이외인 요소에만 적용된다.

## overflow 프로퍼티

overflow 프로퍼티는 자식 요소가 부모 요소의 영역를 벗어났을 때 처리 방법을 정의한다.

visible, hidden, scroll, auto 등의 값이 존재한다.