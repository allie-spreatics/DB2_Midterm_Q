# 프론트엔드 과제 가이드

프론트엔드 과제에 대한 요구사항 및 채점 항목에 대한 안내 가이드입니다.

## 목차

1. [개요](#1-개요)
2. [프로젝트구조](#2-프로젝트-구조)
3. [기능 요구사항 및 배점](#3-기능-요구사항-및-배점)

## 1. 개요

- Todo를 관리하는 프론트엔드 과제입니다.
- 백엔드 연동 없이 프론트엔드로만 구현하면 됩니다.
- 과제는 **10점 만점**이며 미준수 시 감점되는 항목은 별도로 표시해두었으니 반드시 숙지해주세요.

  - 해당 과제의 최저점은 2점 입니다. (기본점수 2점)

- 해당 과제의 평가 요소는 얼마나 예쁘게 구현했는가, 코드가 얼마나 효율적인가 등이 아닌 **평가 가이드에 맞추어 코드를 작성했는가** 이므로 가이드에 따라 과제를 구현해주세요.

- `3.2`문항 을 진행하지 않으면 나머지 과정들을 진행할 수 없습니다. `3.2`문항을 작성하기 어려운 경우 임의로 html을 작성후 나머지 부분을 진행해도 부분점수가 인정됩니다.

## 2. 프로젝트 구조

- 프로젝트 구조는 다음과 같습니다.

```txt
frontend/
ㄴ public/
    ㄴ codingon.png
    ㄴ index.css
    ㄴ index.js
ㄴ index.html
```

- 기본 HTML, CSS, JavaScript 파일을 만들어뒀으니 파일을 추가 삭제하지 않아야 합니다. (\*미준수 시 1점 감점)

### 2.1 index.html

- Todo 애플리케이션의 **구조를 정의**하는 파일입니다.
- `<title>` 태그 내용은 본인 이름을 작성합니다. (\*미준수 시 1점 감점)
  ```html
  <title>김철수</title>
  ```
- HTML 요소에는 `style`, `width`, `height` 속성을 사용하지 않습니다. 꾸미기 속성은 `CSS`를 사용합니다. (\*미준수 시 1점 감점)

### 2.2 public/index.css

- Todo 애플리케이션의 **스타일**을 담당하는 파일입니다.
- 제시된 기능 요구사항 외에는 `margin`, `padding`, `color`, `background-color`, `width`, `height` 등의 속성이 예제와 정확히 일치하지 않아도 됩니다.

### 2.3 public/index.js

- Todo 애플리케이션의 **동작**을 담당하는 파일입니다.
- 기능 요구사항은 `JavaScript` 를 기준으로 작성하지만, `jQuery` 를 사용하여 구현해도 괜찮습니다.
- 이벤트 리스너 등록 방식은 혼합하여 사용하여도 괜찮습니다. 편한 방법으로 구현해주세요.

### 2.4 public/codingon.png

- 헤더 요소 구현 시 필요한 **이미지** 파일입니다.

## 3. 기능 요구사항 및 배점

원활한 평가를 위해 가이드에서 제시하는 네이밍(변수명, 함수명 등)이 있다면 맞춰서 작성해야 합니다. 각 기능별로 배점을 기입해두었습니다.

### 3.1 반응형 레이아웃 (총 배점 2.5점)

- (배점 0.5점) 브라우저 너비가 `540px` 보다 작을 때에는 1단으로 Todo 목록이 보여져야 합니다.
- (배점 0.5점) 브라우저 너비가 `540px` 보다 작을 때에는 헤더의 로고 이미지와 제목(Todo List)이 가로에서 세로 방향으로 배치가 변경됩니다.
- (배점 0.5점) 브라우저 너비가 `540px` 이상 `960px` 미만일 때에는 2단으로 Todo 목록이 보여져야 합니다.
- 브라우저 너비가 `960px` 이상일 때에는,
  - (배점 0.5점) 4단으로 Todo 목록이 보여져야 합니다.
  - (배점 0.5점) 헤더, 입력창, Todo 목록을 포함하는 요소의 최대 너비는 `800px` 입니다.
    > 힌트. `max-width` 속성

> [프론트엔드 구현 예시 보기](https://uncovered-nutmeg-b8e.notion.site/caa79e835f254da9a7d78437cb4ef1de?pvs=4)

### 3.2 초기 Todo 목록 불러오기 (총 배점 2점)

- (배점 1점) `getTodos()` 함수는 `GET` `https://jsonplaceholder.typicode.com/todos` 요청의 응답 결과에서 맨 처음부터 10개의 원소만 잘라내어 투두 목록에 초기 Todo를 표시해야 합니다.
  > 힌트. `slice()` 메서드
- (배점 1점) HTML 문서의 DOM 내용이 완전히 로드되었을 때, 초기 Todo 목록을 불러오는 `getTodos()` 함수가 실행됩니다.
  > 힌트. `DOMContentLoaded` 이벤트

### 3.3 Todo 추가 기능 (총 배점 1.5점)

- (배점 0.5점) `addTodo()` 함수는 새로운 입력창의 Todo를 Todo 목록에 추가하고, 입력창을 초기화합니다.
- (배점 0.5점) 공백이나 빈 문자열의 경우 추가될 수 없습니다.
- (배점 0.5점) `작성` 버튼 클릭 시 `addTodo()` 함수가 실행됩니다.

### 3.5 Todo 삭제 기능 (총 배점 1점)

- (배점 1점) `x` 버튼을 클릭하면 클릭한 버튼을 갖는 Todo 항목이 삭제됩니다.

### 3.6 Todo 완료 기능 (총 배점 1점)

- (배점 0.5점) Todo의 체크박스 클릭 시 폰트 색이 변경되는가
- (배점 0.5점) Todo의 체크박스 클릭 시 취소선이 추가되는가