> 📚Date : 2025.05.13(Tue)

# 한글버전

# 2. HTML

## 2.1 What is HTML?

> Hypertext Markup Language
>
> 마크업 언어, 태그를 이용해서 구조화하는 언어이다.

## 2.2 HTML 기본문법

- html 요소인 `element`는 `opening tag`와 `closing tag`그리고 `content`로 구성된다.
- HTML은 중첩의 구조 nested element를 띈다.

```plaintext
부모 요소 parent/
└── 자식 요소/
    ├── 하위(후손) 요소
    ├── 하위(후손) 요소
    └── 하위(후손) 요소

    * 이떄 구분은 들여쓰기(indent)와 내어쓰기(outdent)로 구분한다.
```

- 속성(attribute)  
   : 요소의 성질과 특징을 정의하는 것으로 추가적 정보를 제공하는 기능을 한다.
- 빈 요소(empty)  
   : content 가 없는 빈 요소로 속성(attribute)만을 소유하고 있다. (예. meta, br, img, input, link)
- 주석(comments)  
   : 개발자에게 코드를 설명하여 개발 환경에 용이하도록 한다. 주석은 화면에 표시하지 않는다.

## 2.3 HTML 기본 태그

### 2.3.1 본문 태그 `<p></p>`

- 본문을 뜻하는 paragraph의 약자로 p를 사용한다.
- 본문을 적기 위한 태그이다.

### 2.3.2 줄 바꿈 태그 `<br>`

- 줄 바꿈

### 2.3.3 목록 태그 `<ol></ol>` , `<ul></ul>`

#### unordered list : `<ul></ul>`

- list : `<li></li>`

```html
<ul>
  <li></li>
  <li></li>
  <li></li>
</ul>
```

#### ordered list : `<ol></ol>`

- type : 1, A, a, I, i
- start : 시작하는 지점
- reversed : 역순으로

```html
<ol start="6" type="1" reversed>
  <li>감자</li>
  <li>고구마</li>
  <li>밤</li>
</ol>
```

- 출력값 :

```plaintext
6. 감자
5. 고구마
4. 밤
```

### 2.3.4 수평 줄 `<hr />`

- 수평으로 된 줄을 그어 준다.

### 2.3.5 문자 꾸미기 태그들

- `<b></b>` : bold
- `<strong></strong>` : 두껍게, Semantic한 의미를 지님
- `<i></i>` : 이탤릭
- `<em></em>` : emphasize 강조, 기울여서 표시
- `<del></del>` : 중간줄
- `<u></u>` : 밑줄

### 2.3.6 이미지 `<img>`

- `src` 해당 이미지의 주소 넣기
- `alt` 이미지가 로드 안될 경우 대신 나오는 이미지에 대한 설명

```html
<img src="./album.png" alt="album image" width="50%" />
```

### 2.3.7 하이퍼링크 `<a>`

- `href` : 링크 주소 입력
- `target` : 해당 링크를 열 방법을 지정
  - \_blank : 새로운 탭에서 링크 열기
  - \_self : 현재 탭에서(기본값)

### 2.3.8 사용자 입력

#### `<form></form>`

`<input>`태그를 감싸준다.

#### `value`

- 사용자가 input 안에 content을 입력했을 때 전달되는 값을 의미한다.

#### `placeholder = "luv@example.com`

- 사용자 입력란에 양식을 보여주기 위하는 등 설명하는 값을 의미한다.

#### `type="button"`

- 버튼을 생성하여 주로 특정 기능을 수행하는 데 사용한다.

#### `type="text"`

- 텍스트를 입력받는 폼을 생성하여 텍스트 값을 입력 받아 전달한다.

#### `type="textarea"`

- 1줄 이상의 텍스트를 입력받아 전달한다.

#### `type="password"`

- 비밀번호를 입력을 위해 사용한다.

#### `type="checkbox"`

- 중복을 허용하여 체크할 때 사용한다.
- name : 체크박스의 이름으로 같은 분류의 체크 박스는 같은 이름으로 설정한다!!
- checked : 화면 최초 로딩 시 선택 된 상태로 로딩된다.
- disabled : 화면에는 출력되지만 체크가 되지 않도록 한다.
- value : 선택했을 때 전달되는 값이다.

#### `type="radio"`

- 여러 선택지 중 단 하나만 선택 가능한 라디오 버튼을 생성한다.
- name : 라디오 버튼들의 이름으로 같은 name을 가지는 버튼들 중에서는 하나만 선택 가능하다. 하나를 선택 시 다른 선택 값은 자동으로 취소된다.
- checked : 화면 최초 로딩 시 선택 된 상태로 로딩된다.
- disabled : 화면에는 출력되지만 체크가 되지 않도록 한다.
- value : 선택했을 때 전달되는 값이다.

#### `type="date"`

- 특정 날짜 (년/월/일)을 선택할 수 있다.

#### `type="datetime-local"`

- 시간까지 선택한다.

#### `type="color"`

- 색을 선택한다. (RGB값)

#### `type="range"`

- 범위를 선택한다.

#### `type="file"`

- 파일을 넣을 수 있다.

### 2.3.9 선택 메뉴를 만드는 `<select></select>`

#### `<select>`

- select 폼을 생성한다.
- `name="example"` select 박스의 이름

#### `<option>`

- select 폼의 옵션 값을 생성한다.
- `value` : 실제적으로 전달 되는 값
- `selected` : 화면 최초 로딩 시 선택 된 값으로 설정한다.
- `disabled` : 옵션은 보이지만 선택을 못하도록 설정한다.

#### `<optgroup label="group1">`

- option을 그룹화한다.
- `lable` : optgroup 이름을 설정한다.

### 2.3.10 테이블 `<table></table>`

`<table border = "1">`
| td | td | td |
| --- | --- | --- |
| td | td | td |
| td | td | td |
`</table>`

#### `<table>`

- 표를 감싸는 태그

#### `<thead>`와 `<tbody>`

- `<thead>`: 제목 줄
- `<tbody>` : 일반 줄 전부를 담고 있는 태그

#### `<tr>`

- 표 내부의 행 table row

#### `<th>`

- 헹 내부의 제목 칸 table head

#### `<td>`

- 행 내부의 일반 칸 table body

##### colspan

: 해당 칸이 점유하는 열의 수를 지정한다.

##### rowspan

: 해당 칸이 점유하는 행의 수를 지정한다.

#### `<caption>`

- 표에 대한 설명을 적는다.

```html
<table border="1">
  <caption style="caption-side: bottom">
    캡션
  </caption>
  <thead>
    <tr>
      <th>학교</th>
      <th>창립년도</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>서울대학교</td>
      <td>1946년</td>
    </tr>
  </tbody>
</table>
```

# English version

# 2. HTML

## 2.1 What is HTML?

> **HTML (Hypertext Markup Language)**
>
> A markup language that structures content using tags.

---

## 2.2 Basic HTML Syntax

- An HTML **element** consists of an **opening tag**, **content**, and a **closing tag**.
- HTML supports **nested structures** (elements within elements).

```plaintext
Parent Element
└── Child Element
    ├── Descendant Element
    ├── Descendant Element
    └── Descendant Element

* Nesting is visually represented using indentation (indent/outdent).
```

- **Attribute**: Provides additional information about an element.
- **Empty Element**: Elements with no content (e.g., `<meta>`, `<br>`, `<img>`, `<input>`, `<link>`).
- **Comment**: Non-visible note in code, used for documentation.

```html
<!-- This is a comment -->
```

---

## 2.3 Common HTML Tags

### 2.3.1 Paragraph Tag `<p>`

- Used for writing paragraphs.

### 2.3.2 Line Break `<br>`

- Inserts a line break.

### 2.3.3 Lists `<ol>`, `<ul>`

#### Unordered List `<ul>`

```html
<ul>
  <li>Item</li>
  <li>Item</li>
</ul>
```

#### Ordered List `<ol>`

- Attributes: `type`, `start`, `reversed`

```html
<ol start="6" type="1" reversed>
  <li>Potato</li>
  <li>Sweet Potato</li>
  <li>Chestnut</li>
</ol>
```

**Output:**

```plaintext
6. Potato
5. Sweet Potato
4. Chestnut
```

### 2.3.4 Horizontal Line `<hr />`

- Draws a horizontal line.

### 2.3.5 Text Formatting Tags

- `<b>`: Bold
- `<strong>`: Bold with semantic emphasis
- `<i>`: Italic
- `<em>`: Emphasized (italic with meaning)
- `<del>`: Strikethrough
- `<u>`: Underline

### 2.3.6 Image Tag `<img>`

```html
<img src="./album.png" alt="Album Image" width="50%" />
```

- `src`: Image path
- `alt`: Description if image can't be loaded

### 2.3.7 Hyperlink Tag `<a>`

- `href`: Destination URL
- `target`: Link behavior (`_blank` for new tab, `_self` for same tab)

### 2.3.8 User Input

#### Form Container `<form>`

- Wraps input elements

#### Input Types:

- `type="text"`: Single-line text
- `type="password"`: Password field
- `type="checkbox"`: Multiple selections
- `type="radio"`: Single choice from options
- `type="date"`: Date picker
- `type="datetime-local"`: Date & time picker
- `type="color"`: Color picker
- `type="range"`: Range slider
- `type="file"`: File upload
- `type="button"`: Button (no submit)

#### Additional Attributes:

- `value`: Value passed on submit
- `placeholder`: Hint text inside input
- `checked`: Pre-selected option
- `disabled`: Non-editable input

### 2.3.9 Dropdown Menu `<select>`

```html
<select name="example">
  <option value="1">Option 1</option>
  <option value="2" selected>Option 2</option>
</select>
```

- `<optgroup label="Group">`: Groups options

### 2.3.10 Tables `<table>`

#### Basic Table

```html
<table border="1">
  <caption style="caption-side: bottom">
    Table Caption
  </caption>
  <thead>
    <tr>
      <th>School</th>
      <th>Founded</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Seoul National University</td>
      <td>1946</td>
    </tr>
  </tbody>
</table>
```

#### Table Elements

- `<thead>`: Header rows
- `<tbody>`: Data rows
- `<tr>`: Table row
- `<th>`: Header cell
- `<td>`: Data cell
- `colspan`: Span multiple columns
- `rowspan`: Span multiple rows
- `<caption>`: Table description
