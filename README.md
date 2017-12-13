> 이 문서는 크게 두 가지로 나뉘어져 있습니다. 
>
>1. 마크다운 문법: 포스트 작성 양식인 마크다운 문법을 정리했습니다.
>2. 블로그 관리 길라잡이: 블로그 사이트를 어떻게 관리하는지 설명해 놓았습니다. 

# 1. 마크다운 문법

## 제목(Heading)

'#'의 개수에 따라 글자의 크기가 달라집니다. 6개까지 사용 가능합니다.
```
# Heading
## Heading
### Heading
#### Heading
##### Heading
###### Heading
```
# Heading
## Heading
### Heading
#### Heading
##### Heading
###### Heading

## 본문(Paragraph)

본문은 텍스트를 그대로 작성하면 됩니다.
```
Lorem ipsum dolor sit amet, consectetur adipisicing elit
```
Lorem ipsum dolor sit amet, consectetur adipisicing elit

## 인용(Blockquotes)

인용은 `>`넣어서 작성합니다.

```
> Lorem ipsum dolor sit amet, consectetur adipisicing elit
>> Lorem ipsum dolor sit amet, consectetur adipisicing elit
```
> Lorem ipsum dolor sit amet, consectetur adipisicing elit
>> Lorem ipsum dolor sit amet, consectetur adipisicing elit

## 리스트

### 순서가 없는 리스트(Unordered List)

`*`또는 `-`를 사용해서 순서가 없는 리스트를 작성할 수 있습니다. tab 또는 2칸 띄어쓰기를 통해 중첩된 항목을 작성할 수도 있습니다.

```
* Frontend
  * HTML
  * CSS
  * JavaScript
    * Vue.js

- Frondend
  - HTML
  - CSS
  - JavaScript
    - Vue.js
```

* Frontend
  * HTML
  * CSS
  * JavaScript
    * Vue.js

- Frondend
  - HTML
  - CSS
  - JavaScript
    - Vue.js

### 순서가 있는 리스트(Ordered List)

```
1. Frontend
    1. HTML
    2. CSS
    3. JavaScript
        1. Vue.js
2. Backend
```

1. Frontend
    1. HTML
    2. CSS
    3. JavaScript
        1. Vue.js
2. Backend

## 수평선(Horizontal Rules)

문단과 문단 사이를 나눌 때 사용되는 수평선입니다.

```
* * *
***
*****
- - -
---------------------------------------
```

* * *
***
*****
- - -
---------------------------------------

## 링크(Links)

하이퍼링크입니다. title은 생략이 가능합니다.

```
[example](http://example.com "title")

검색엔진은 [구글](https://www.google.com "구글")을 사용합니다.
```

[example](http://example.com "title")

검색엔진은 [구글](https://www.google.com "구글")을 사용합니다.

## 강조(Emphasis)

이탤릭체는 `*`, `_`를 쓰고 볼드체는 `**`, `__`를 사용합니다. 취소선은 `~~`를 사용합니다.

```
*이탤릭체*
_이탤릭체_
```

_이탤릭체_

```
**볼드체**
__볼드체__
```

__볼드체__

```
~~취소~~한 텍스트
```

~~취소~~한 텍스트

## 이미지 삽입(Images)

이미지를 본문 중간에 삽입할 수도 있습니다. 이미지에 문제가 생겨 나오지 않는 경우에 이미지를 대체할 텍스트를 삽입할 수도 있습니다. 링크 또는 로컬의 이미지 파일을 연결하여 사용합니다.

```
![대체 텍스트](/경로)
![대체 텍스트](링크)
```

```
![logo](/assets/logo.png)
```
![logo](/assets/logo.png)

```
![Github](https://assets-cdn.github.com/images/modules/open_graph/github-octocat.png)
```

![Github](https://assets-cdn.github.com/images/modules/open_graph/github-octocat.png)

# 2. 블로그 관리 길라잡이

블로그를 관리하기 위해서 다음 세 사이트를 이용합니다. 

* __깃허브(github[])__: 블로그 사이트가 될 파일들이 저장되어 있습니다.
* __디스커스(disqus[])__: 댓글을 관리합니다.
* __구글 애널리틱스(google analytics[])__: 블로그 방문자 분석을 합니다.

## 깃허브(github)

깃허브의 USERNAME.github.io 저장소(repository)에 들어가 보면 여러 파일들이 있습니다. 모든 파일을 알 필요는 없고 몇 가지만 알고 사용하면 됩니다. 사용하게 될 파일은 다음 세 가지입니다.

* `_config.yml` 파일: 사이트 전반에 관한 설정을 여기서 합니다.
* `_posts` 폴더: 모든 블로그 포스트를 담고 있는 폴더입니다. 폴더 안의 파일은 `.md`확장자를 붙여주세요
* `assets` 폴더: 블로그에 쓰일 사진이나 동영상 등을 보관합니다.

### 환경설정: _config.yml

블로그 제목, 이메일 등의 정보를 `_config.yml` 파일에 입력해 놓으면 모든 블로그 페이지에서 필요할 때 그 정보를 알아서 읽고 사용합니다. 블로그 운영자에 따라 아래의 내용만 바꿔서 사용하면 됩니다.

#### __site settings__
 ```yml
 # Site settings
 title: 농업블로그
 subtitle: 농업블로그입니다.
 email: agriculture@gmail.com
 name: 홍길동
 description: 농업블로그에 관한 설명입니다.
 # Base URL of site (i.e. /blog). It should always start with a slash,
 # and never end with a slash. Set it to a blank value if hosting at the
 # root of your server.
 baseurl: "" # the subpath of your site, e.g. /blog/
 url: "" # the base hostname & protocol for your site
 cover: "/assets/header_image.jpg"
 logo: "/assets/logo.png"
 ```  
 1. `title`: 블로그의 제목입니다. 홈 페이지 상단의 제목과 기본 탭 타이들로 쓰입니다.
 2. `subtitle`: 블로그의 부제입니다. 홈 페이지 상단의 제목 밑에 부제로 쓰입니다.
 3. `email`: 블로그를 대표하는 사람의 이메일입니다. 모든 페이지 하단에 표시됩니다.
 4. `name`: 블로그를 대표하는 사람의 이름입니다. 웹페이지 화면에는 직접 나오지 않지만 블로그에 대한 정보로서 사이트가 저장하고 있습니다.
 5. `description`: 블로그에 대한 설명으로 모든 페이지 하단에 기제됩니다.
 6. `baseurl` `url`: 아무것도 입력하지 않아도 됩니다.
 7. `cover`: 블로그 홈 페이지의 커버 사진입니다. 사진이 저장되어 있는 경로를 입력해줍니다.
 8. `logo`: 로고입니다. 로고 사진 파일이 저장되어 있는 경로를 입력해줍니다. 

#### __social__
 ```yml
 # social:
 #   - name: Twitter                         # Name of the service
 #     icon: twitter                         # Font Awesome icon to use (minus fa- prefix)
 #     username: "@TheBenCentra"             # (User) Name to display in the footer link
 #     url: https://twitter.com/TheBenCentra # URL of your profile (leave blank to not display in footer)
 #     desc: Follow me on Twitter            # Description to display as link title, etc
 #     share: true                           # Include in the "Share" section of posts
 social:
  - name: Twitter
    icon: twitter
    username: TheBenCentra"/assets/instacode.png"
    url: https://twitter.com/TheBenCentra
    desc: Follow me on Twitter
    share: true

  - name: Facebook
    icon: facebook
    username: thebencentra
    url:
    desc: Friend me on Facebook
    share: true
 ```
 불필요한 sns 서비스는 삭제해도 되고 사용할 sns는 다음을 설정해두면 됩니다.

 1. `username`: sns 유저 이름을 입력합니다. 모든 페이지 하단의 contact에 보이게 됩니다.
 2. `url`: sns 주소를 입력합니다. 페이지 하단의 소셜 링크 주소입니다.
 3. `desc`: 소셜링크에 마우스를 가져다대면 나오는 문구입니다.
 4. `share`: `true` 또는 `false`만 입력 가능합니다. 블로그 포스트의 공유 버튼을 생성할 지 결정합니다.
 
### 포스트 작성하기: _posts

#### 파일 형식

포스트를 작성하기 위해서 먼저 `_posts`폴더에 새 파일을 생성합니다. 이 때 중요한 것은 파일의 이름입니다. 파일의 이름은 반드시 다음 형식에 맞춰야 합니다.
```
YEAR-MONTH-DAY-title.MARKUP
```
`YEAR`는 네 자리의 숫자, `MONTH`와 `DAY`는 두 자리 숫자이고, 확장자 부분의 `MARKUP`은 `.md`를 입력하면 됩니다. 올바른 예시를 들면 다음과 같습니다.
```
2017-12-11-how-to-write-a-blog.md
```

#### 머리말

모든 블로그 포스트 파일 첫 부분에는 머리말을 작성해야 합니다. 머리말은 포스트의 기본 정보를 담고 있습니다. 머리말은 반드시 올바른 형식으로 작성되어야 하며, 대시문자 3개로 감싸서 파일의 맨 첫 부분에 위치해야 합니다. 여러 머리말을 설정할 수 있지만 우리가 사용할 머리말은  다음과 같습니다.
```
---
layout: post
title: welcome to my blog
date: 2017-12-11 17:19:42
author: BABA
categoris: agriculture
tags: agriculture, agri
cover: /assets/picture.png
---
```
1. `layout`: 무조건 `post`를 입력합니다.
2. `title`: 포스트의 제목입니다.
3. `date`: 포스트 작성 시각을 입력합니다. 포스트를 올바르게 정렬하기 위해 사용되고 시간, 분, 초는 선택사항입니다.
4. `author`: 포스트의 작성자입니다. 웹페이지에 직접적으로 드러나지는 않습니다. 단지 포스트의 정보로서 가지고 있을 뿐입니다. 선택사항입니다.
5. `categories`: 포스트의 카테고리를 입력합니다. 이 카테고리에 따라 자동으로 포스트가 분류됩니다.
6. `tags`: 포스트의 태그입니다.
7. `cover`: 포스트의 커버 사진입니다. 선택사항으로, 있으면 배경 이미지로 쓰이고 없으면 글만 나타납니다.

#### 마크다운으로 작성하기

모든 포스트 글은 마크다운 문법에 따라 작성되어야 합니다. 마크다운 문법은 읽고 쓰기 편하고, 쉽게 HTML코드로 변환시킬 수 있습니다. 

마크다운 문법 정리는 이 문서 제일 첫 부분에 있습니다.

### 이미지와 자원 보관하기

웹페이지에서 사용된 이미지 등은 모두 `_assets`폴더에 보관합니다. 그리고 각 자원의 경로만 알고 사용하면 됩니다.

예를 들어 `_assets` 폴더 밑에 `image`라는 폴더를 만들고 그 안에 `img.png`라는 파일이 있으면 `/_assets/image/img.png`를 경로로 사용하면 됩니다. `_assets` 폴더 바로 밑에 `main-img.png`라는 파일을 사용할 때 경로는 `/_assets/main-img.png`가 됩니다.
