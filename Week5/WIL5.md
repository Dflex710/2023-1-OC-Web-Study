# Week5

**HTML**

1. HTML5의 기본 문법

HTML5 문서는 다음과 같은 구조로 작성됩니다:

```
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Hello World</title>
  </head>
  <body>
    <h1>Hello World</h1>
    <p>안녕하세요! HTML5</p>
  </body>
</html>

```

위의 예시는 기본적인 HTML5 문서 구조를 보여줍니다. 문서는 `<!DOCTYPE html>`로 시작하여 HTML5 문서임을 지정합니다. 그 다음 `<html>` 태그와 `</html>` 태그 사이에 실제적인 HTML 문서 내용이 작성됩니다.

`<head>`와 `</head>` 사이에는 문서의 제목(title), 외부 파일 참조, 메타데이터 설정 등이 위치하며, 이 정보들은 브라우저에 표시되지 않습니다.

웹브라우저에 실제로 출력되는 모든 내용은 `<body>`와 `</body>` 사이에 위치합니다. 위 예시에서는 `<h1>` 태그로 "Hello World"라는 제목을, `<p>` 태그로 "안녕하세요! HTML5"라는 문장을 작성했습니다.

HTML 문서는 요소(Element)들로 구성됩니다. 요소는 시작 태그(start tag), 종료 태그(end tag), 그리고 태그 사이에 위치한 내용(content)로 구성됩니다. 요소들의 집합으로 HTML 문서가 구성됩니다.

빈 요소(Empty element 또는 Self-Closing element)는 content를 가지지 않는 요소입니다. 이러한 요소는 종료 태그 대신 단일 태그로 표현됩니다. 빈 요소는 content가 없으며 어트리뷰트(Attribute)만을 가질 수 있습니다. 몇 가지 대표적인 빈 요소는 다음과 같습니다:

- `<br>`: 줄바꿈 요소
- `<hr>`: 수평선 요소
- `<img>`: 이미지 요소
- `<input>`: 입력 요소
- `<link>`: 외부 리소스 연결 요소
- `<meta>`: 메타데이터 요소

어트리뷰트는 각 요소에서 사용할 수 있는 특정한 속성들이 존재하지만, 모든 HTML 요소가 공통으로 사용할 수 있는 어트리뷰트도 있습니다. 이를 글로벌 어트리뷰트(Global Attribute)라고 합니다. 일반적으로 모든 요소에서 사용할 수 있는 몇 가지 글로벌 어트리뷰트는 다음과 같습니다:

- `id`: 유일한 식별자를 요소에 지정합니다. 중복 지정이 불가능합니다.
- `class`: 스타일시트에서 정의된 클래스를 요소에 지정합니다. 중복 지정이 가능합니다.
- `hidden`: 요소를 화면에서 숨깁니다. CSS의 `hidden`과는 다르게 의미적으로도 브라우저에 노출되지 않습니다.
- `lang`: 요소의 언어를 지정합니다. 검색 엔진이 웹페이지의 언어를 인식할 수 있게 합니다.
- `style`: 요소에 인라인 스타일을 지정합니다.
- `tabindex`: 사용자가 키보드로 페이지를 탐색할 때 이동 순서를 지정합니다.
- `title`: 요소에 대한 제목을 지정합니다.

주석(Comments)은 주로 코드를 설명하기 위해 개발자가 사용하는 기능입니다. 브라우저는 주석을 화면에 표시하지 않습니다. 주석은 `<!--`로 시작하여 `-->`로 종료되는 형식으로 작성됩니다.
<!--주석은 화면에 표시되지 않는다.-→

1. 시멘틱 요소와 결합엔진

**시맨틱 태그란 브라우저, 검색엔진, 개발자 모두에게 콘텐츠의 의미를 명확히 설명하는 역할을 한다.** 시맨틱 태그에 의해 컴퓨터가 HTML 요소의 의미를 보다 명확히 해석하고 그 데이터를 활용할 수 있는 시맨틱 웹이 실현될 수 있다.

**시맨틱 웹이란 웹에 존재하는 수많은 웹페이지들에 메타데이터(Metadata)를 부여하여, 기존의 잡다한 데이터 집합이었던 웹페이지를 ‘의미’와 ‘관련성’을 가지는 거대한 데이터베이스로 구축하고자 하는 발상이다.**

HTML 요소는 non-semantic 요소, semantic 요소로 구분할 수 있다.

**non-semantic 요소**div, span 등이 있으며 이들 태그는 content에 대하여 어떤 설명도 하지 않는다.**semantic 요소**form, table, img 등이 있으며 이들 태그는 content의 의미를 명확히 설명한다,

다음은 HTML5에서 새롭게 추가된 시맨틱 태그이다.

| tag | Description |
| --- | --- |
| header | 헤더를 의미한다 |
| nav | 내비게이션을 의미한다 |
| aside | 사이드에 위치하는 공간을 의미한다 |
| section | 본문의 여러 내용(article)을 포함하는 공간을 의미한다 |
| article | 분문의 주내용이 들어가는 공간을 의미한다 |
| footer | 푸터를 의미한다 |

1. **웹페이지의 구성하는 기본 태그**

‘’**문서 형식 정의, html, head, body’’**

**문서 형식 정의(Document Type Definition, DTD) 태그**는 출력할 웹 페이지의 형식을 브라우저에게 전달한다. 문서의 최상위에 위치해야 하며 대소문자를 구별하지 않는다. 문서별 기술 양식은 아래와 같다.

**html 태그**는 모든 HTML 요소의 부모 요소이며 웹페이지에 단 하나만 존재한다. 즉, 모든 요소는 html 요소의 자식 요소이며 html 요소 내부에 기술해야 한다. 단 `<!DOCTYPE>`는 예외이다.

head 요소는 [메타데이터](https://ko.wikipedia.org/wiki/%EB%A9%94%ED%83%80%EB%8D%B0%EC%9D%B4%ED%84%B0)를 포함하기 위한 요소이며 웹페이지에 단 하나만 존재한다. 메타데이터는 HTML 문서의 title, style, link, script에 대한 데이터로 화면에 표시되지 않는다. head 요소에는 메타데이터 이외의 화면에 표시되는 일체의 요소를 포함시킬 수 없다.
1) **title tag**: title 요소는 문서의 제목을 정의한다. 정의된 제목은 브라우저의 탭에 표시된다.
2) **style tag**: style 요소에는 HTML 문서를 위한 style 정보를 정의한다.
3) **link tag**: link 요소에는 외부 리소스와의 연계 정보를 정의한다. 주로 HTML과 외부 CSS 파일을 연계에 사용된다.
4) ****script tag:**** script 요소에는 client-side JavaScript를 정의한다.
5) ****meta tag:**** meta 요소는 description, keywords, author, 기타 메타데이터 정의에 사용된다. 메타데이터는 브라우저, 검색엔진(keywords) 등에 의해 사용된다.

**body 태그**는 HTML 문서의 내용을 나타내며 웹페이지에 단 하나만 존재한다. 메타데이터를 제외한 웹페이지를 구성하는 대부분의 요소가 body 요소 내에 기술된다.

1. **텍스트 관련 태그**

**1) 제목(Headings)태그**

Heading 태그는 제목을 나타낼 때 사용하며 h1에서 h6까지의 태그가 있다. h1이 가장 중요한 제목을 의미하며 글자의 크기도 가장 크다.

[시맨틱 웹](https://poiemaweb.com/html5-semantic-web)의 의미를 살려서 제목 이외에는 사용하지 않는 것이 좋다. 검색엔진은 제목 태그를 중요한 의미로 받아들일 가능성이 크다.

**2) 글자형태(Text Formatting) 태그**

**#2.1 b**

bold체를 지정한다. 제목 태그와 같이 의미론적(Semantic) 중요성의 의미는 없다.

**#2.2 strong**

b tag와 동일하게 bold체를 지정한다. 하지만 의미론적(Semantic) 중요성의 의미를 갖는다.

표현되는 외양은 b tag와 동일하지만 웹표준을 준수하고자 한다면 strong를 사용하는 것이 바람직하다.

**#2.3 i**

Italic체를 지정한다. 의미론적(Semantic) 중요성의 의미는 없다.

**#2.4 em**

emphasized(강조, 중요한) text를 지정한다. i tag와 동일하게 Italic체로 표현된다. 의미론적(Semantic) 중요성의 의미를 갖는다.

**#2.5 small**

small text를 지정한다.

**#2.6 mark**

highlighted text를 지정한다.

**#2.7 del**

deleted (removed) text를 지정한다.

**#2.8 ins**

inserted (added) text를 지정한다.

**#2.9 sub / sup**

sub 태그는 subscripted(아래에 쓰인) text를 sup 태그는 superscripted(위에 쓰인) text를 지정한다.

**3) 본문 태그**

**#3.1 p**

단락 (Paragraphs)을 지정한다.

**#3.2 br**

br tag는 (강제)개행 (line break)을 지정한다. br tag는 빈 요소(empty element)로 종료태그가 없다.

HTML에서는 1개 이상의 연속된 공백(space)을 삽입하여도 1개의 공백으로 표시된다. 1개 이상의 연속된 줄바꿈(enter)도 1개의 공백으로 표시된다.

**#3.3 pre**

형식화된(preformatted) text를 지정한다. pre 태그 내의 content는 작성된 그대로 브라우저에 표시된다.

**#3.4 hr**

수평줄을 삽입한다.

**#3.5 q**

짧은 인용문(quotation)을 지정한다. 브라우저는 인용부호(큰따옴표/quotation marks)로 q 요소를 감싼다.

**#3.6 blockquote**

긴 인용문 블록을 지정한다. 브라우저는 blockquote 요소를 들여쓰기한다. css를 이용하여 다양한 style을 적용할 수 있다.

**CSS**

**1. 셀렉터 (Selector, 선택자)**

CSS는 HTML 요소의 style(design, layout etc)을 정의하는데 사용된다. 이를 위해서 선행되어야하는 것은 **스타일을 적용하고자 하는 HTML 요소를 선택**할 수 있어야 한다.

셀렉터는 스타일을 적용하고자 하는 HTML 요소를 선택하기 위해 CSS에서 제공하는 수단이다.

![https://poiemaweb.com/img/css-syntax.png](https://poiemaweb.com/img/css-syntax.png)

CSS Rule Set

위와 같은 구문을 Rule Set(또는 Rule)이라 하며 셀렉터에 의해 선택된 특정 HTML 요소를 어떻게 렌더링(Rendering)할 것인지 브라우저에 지시하는 역할을 한다. 위의 CSS Rule set은 HTML 문서에 속해 있는 셀렉터를 통해 모든 h1 요소를 선택한 후 선택된 h1 요소의 스타일을 선언 블록에서 정의하고 있다.

이와 같은 Rule Set의 집합을 스타일시트(Style Sheet)라 한다.

**2. 프로퍼티 (Property / 속성)**

셀렉터로 HTML 요소를 선택하고 {} 내에 프로퍼티(속성)와 값을 지정하는 것으로 다양한 style을 정의할 수 있다. 프로퍼티는 [표준 스펙](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference#Keyword_index)으로 이미 지정되어 있는 것을 사용하여야하며 사용자가 임의로 정의할 수 없다. 여러 개의 프로퍼티를 연속해서 지정할 수 있으며 세미콜론(;)으로 구분한다.

**3. 값 (Value / 속성값)**

셀렉터로 지정한 HTML 요소에 style을 적용하기 위해 프로퍼티를 사용했다. 프로퍼티의 값은 해당 프로퍼티에 사용할 수 있는 값을 “키워드”나 “크기 단위” 또는 “색상 표현 단위” 등의 [특정 단위](https://poiemaweb.com/css3-units)로 지정하여야 한다.

**4. HTML과 CSS의 연동**

HTML은 CSS를 포함할 수 있다. CSS를 가지고 있지 않은 HTML은 브라우저에서 기본으로 적용하는 CSS(user agent stylesheet)에 의해 렌더링된다.

CSS와 HTML을 연동하는 방법은 다음과 같다.

**#4.1 Link style**

HTML에서 외부에 있는 CSS 파일을 로드하는 방식이다. 가장 일반적으로 사용된다.

**#4.2 Embedding style**

HTML 내부에 CSS를 포함시키는 방식이다. 매우 간단한 웹페이지의 경우는 문제될 것이 없겠지만 Link style을 사용하는 편이 좋다. HTML과 CSS는 서로 역할이 다르므로 다른 파일로 구분되어 작성하고 관리되는 것이 바람직하다.

참고로 poiemaweb의 예제들 대부분은 Embedding style로 작성되었다. 이는 HTML과 CSS를 한번에 참조할 수 있는 학습에 편한 방식을 취한 것 뿐이다.

**#4.3 Inline style**

HTML요소의 style 프로퍼티에 CSS를 기술하는 방식이다. JavaScript가 동적으로 CSS를 생성할 때 사용하는 경우가 있다. 하지만 일반적인 경우 Link style을 사용하는 편이 좋다.

**5. Reset CSS 사용하기**

모든 웹 브라우저는 디폴트 스타일(브라우저가 내장하고 있는 기본 스타일)을 가지고 있어 CSS가 없어도 작동한다. 그런데 웹브라우저에 따라 디폴트 스타일이 상이하고 지원하는 tag나 style도 제각각이어서 주의가 필요하다.

Reset CSS는 기본적인 HTML 요소의 CSS를 초기화하는 용도로 사용한다. 즉, 브라우저 별로 제각각인 디폴트 스타일을 하나의 스타일로 통일시켜 주는 역할을 한다.

자주 사용되는 Reset CSS는 다음과 같다.

- [Eric Meyer’s reset](http://meyerweb.com/eric/tools/css/reset/)
- [normalize.css](https://necolas.github.io/normalize.css/)

다음은 Eric Meyer’s reset css이다. 이것을 기준으로 사용자의 CSS를 완성해 나가는 방법은 매우 유용하다.

**2.2 셀렉터 부터의 내용은 너무나 방대하고 더이상의 내용정리는 불필요하다 판단하여 여기서 마치겠습니다. 모든 내용을 다 읽어본 결과 모든 내용이 다 필요하고 중요한 상식들이라 지나치기가 어려웠습니다. 해서 여러번 복습하고 html의 내용은 전부 첨가하는 것으로 과제를 마치겠습니다.**