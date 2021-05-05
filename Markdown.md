이 문서에서 기술하는 '탭'이라 하면 띄어쓰기 4칸을 의미한다.

일반적으로는 4칸이긴 하지만 어떤 사용자는 '탭'이 띄어쓰기 2칸이다. 또한 같은 사용자라 하더라도 어떨 때는 4칸이였다가 어떨 때는 2칸으로 되기도 한다. 그래서 markdown을 사용하기 전에 직접 탭을 한번 입력해봐서 확인을 해봐야 한다.

"연속으로 입력한다."라 하면 띄어쓰기 같은 공백 문자 없이 입력하는것을 뜻한다.

# Headings

특정 줄을 제목으로 설정할 수 있는 기능이며, `#`을 이용해서 설정할 수 있다. `#`의 갯수가 많을수록 강조가 약해진다. 예시는 다음과 같다.

    # Headings

->

# Headings<br><br>

    ## Headings

->

## Headings<br><br>

    ### Headings ->

->

### Headings <br><br>

`#` 대신 제목으로 설정하려는 글 밑에 `=`(강한 강조), `-`(약한 강조)를 연속으로 여러번 입력함으로서 강조할 수 있다. 예시는 다음과 같다. `=`과 `-`의 갯수는 1개 이상이면 몇개를 쓰든 상관없다.

    Headings level 1
    =============

->

# Headings level 1

    Headings level 2
    -----------------

->

## Headings level 2

<br><br>
단 `#`으로 제목을 설정할 경우에는 반드시 `#` 치고 한칸 띄워야 한다. 다음과 같이 하면 안된다.

    #Headings

-> #Headings

제대로 강조되지 않는다!

# Paragraph

문단을 나누는 기능이며, `엔터` 두 번 이상 하면서 간단하게 문단을 나눌 수 있다. 예시는 다음과 같다.

    I really like using Markdown.(엔터)(엔터) I think I'll use it to format all of my documents from now on.

->

I really like using Markdown.

I think I'll use it to format all of my documents from now on.<br><br>

단 문단 앞에 스페이스나 탭을 입력하면 안된다. 오직 엔터키만 입력해야 한다.

# Line Breaks

`엔터`를 이용해서 개행하는 것은 여러번 할 수 없다. 추가로(두번 이상) 개행을 하기 위해서는 개행을 하고자 하는 자리에 `스페이스`를 두번(혹은 그 이상) 입력하거나 `<br>`을 입력하면 된다.  
`스페이스`는 몇번을 입력하더라도 추가 개행이 1줄만 개행이 되지만 `<br>`은 한번 쓸때마다 한번 개행이 된다. 즉 `<br>`은 여러 줄을 개행을 할 수 있다. 예시는 다음과 같다.<br><br>

    This is the first line.(스페이스)(스페이스)(엔터)
    And this is the second line.<br>

또는<br>

    This is the first line.<br>(엔터)
    And this is the second line.<br><br>

->

This is the first line.<br>

And this is the second line.<br><br>

문단 맨 뒤에 `\`를 붙여서 개행을 할 수 있지만 그것을 지원하지 않는 Markdown application이 존재하기에 이러한 방법은 추천하지 않는다.<br><br>

# Emphasis

특정 구문을 강조하기 위해서 사용되며, Markdown에서의 강조 기능은 3가지가 있다.  
-> 글씨 굵게 하기, 글씨 기울이기, 글씨 굵게 하면서 기울이기<br><br>

## 글씨 굵게 하기

강조하고자 하는 구문에 `**`나 `__`을 붙이면 된다. `*`나 `_`를 연속으로 2번씩만 입력하면 된다. 예시는 다음과 같다.<br><br>

    I just love **bold text**.
    I just love __bold text__.

-> I just love **bold text**.<br><br>

단 `__` 을 이용해서 강조할 경우에는 `__` 앞뒤로 띄어쓰기가 되었어야 한다. 예시로 다음과 같은 사용법은 잘못된 사용법이다.<br><br>

    Love**is**bold

올바르게 쓰려면 `__`앞뒤로 띄어쓰기를 하거나 띄어쓰기를 못한다면 `__`대신 `**`을 사용해야 한다.<br><br>

## 글씨 기울이기

강조하고자 하는 구문에 `*`나 `_`을 붙이면 된다. **굵게 하는것은 `*`나 `_`을 두번 입력했지만, 기울이는 것은 한 번만 입력해야 한다.** 예시는 다음과 같다.<br><br>

    Italicized text is the *cat's meow*.
    Italicized text is the _cat's meow_.

-> Italicized text is the _cat's meow_.<br><br>

글씨 기울이는 강조도 굵게 강조하는것과 마찬가지로, `_`을 쓰게 된다면 앞뒤로 띄어쓰기를 해야한다. 그렇지 못한다면 `*`을 써야한다. 즉 아래와 같은 사용법은 잘못된 사용법이다.<br><br>

-> A_cat_meow<br><br>

## 글씨 기울이고 굵게 하기

강조하고자 하는 구문에 `***` 또는 `___`을 입력하면 된다. 즉 `*`나 `_`을 연속으로 세 번 입력하면 된다. **특이한 점은 `*` 또는 `_`을 혼용해서 총 3번 입력해도 된다는 것이다. `**\_`, `\*\_\_` 처럼 입력해도 된다는 것이다.`\*\*` 예시는 다음과 같다.<br><br>

    This text is ***really important***.
    This text is ___really important___.
    This text is **_really important_**.
    This text is __*really important*__.

-> This text is **_really important_**.<br><br>

이 강조도 앞선 강조와 마찬가지로 `___`(`_`을 3번 입력)을 이용해서 강조할경우, 앞뒤로 띄어쓰기를 해야한다는 것이다. 그렇지 못할 경우 `*`을 이용해야 한다.<br><br>

# Blockquotes

한 단락의 인용물을 표시하는데 사용되며, 그 줄 맨 앞에 `>`을 붙이면 된다. 예시는 다음과 같다.<br><br>

    > Dorothy followed her through many of the beautiful rooms in her castle.

->

> Dorothy followed her through many of the beautiful rooms in her castle.

<br><br>

# Blockquotes with Multiple Paragraphs

여러 단락의 인용물을 표시하는데 사용되며, 인용하고자 하는 단락과 그 단락 사이 맨 앞에 `>`을 추가하면 된다. 예시는 다음과 같다.<br><br>

    > Dorothy followed her through many of the beautiful rooms in her castle.
    >
    > The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

->

> Dorothy followed her through many of the beautiful rooms in her castle.
>
> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

<br><br>

# Nested Blockquotes

인용문 내에 또 다른 인용문이 들어갈 수 있다. 인용문 내에 넣고자 하는 또 다른 인용문에는 `>`을 두번(`>>`) 붙여주면 된다. 예시는 다음과 같다.<br><br>

    > Dorothy followed her through many of the beautiful rooms in her castle.
    >
    >> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

->

> Dorothy followed her through many of the beautiful rooms in her castle.
>
> > The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

<br><br>

# Blockquotes with Other Elements

인용문 내에 또다른 markdown 요소(Emphasis 등)을 추가할 수 있다. `>`가 있는 문단에 넣고자 하는 요소를 대입하면 된다. 예시는 다음과 같다.<br><br>

    > ### The quarterly results look great!
    >
    > - Revenue was off the chart.
    > - Profits were higher than ever.
    >
    > _Everything_ is going according to \*\*plan\*\*.

->

> ### The quarterly results look great!
>
> - Revenue was off the chart.
> - Profits were higher than ever.
>
>   _Everything_ is going according to **plan**.

# Lists

## Ordered Lists

순서가 있는 리스트를 만들기 위해서 사용된다. 각 문단 앞에 **"자연수."**(`1.` 또는 `2.` 등)를 붙이면 된다. 숫자는 꼭 연속일 필요는 없으며, 숫자를 중복으로 사용할 수 있다. 하지만 시작은 반드시 1부터 시작해야 한다. 예시는 다음과 같다. <br><br>

    1. First item
    2. Second item
    3. Third item
    4. Fourth item

    1. First item
    1. Second item
    1. Third item
    1. Fourth item

    1. First item
    8. Second item
    3. Third item
    5. Fourth item

->

1. First item
2. Second item
3. Third item
4. Fourth item <br><br>

또한 번호가 붙여진 리스트 아래에 또 다른 리스트를 생성할 수 있다. 4번의 띄어쓰기(1번의 탭)를 통해서 생성할 수 있다. 예시는 다음과 같다.<br><br>

    1. First item
    2. Second item
    3. Third item
        1. Indented item
        2. Indented item
    4. Fourth item

->

1. First item
2. Second item
3. Third item
   1. Indented item
   2. Indented item
4. Fourth item<br><br>

이 때 숫자 뒤에는 `.`(온점)을 붙이는게 좋다. 온점 대신 괄호(&nbsp; `)`&nbsp; ) 같은 것을 붙이면 어떤 Markdown applications는 이것을 리스트로 인식을 못할 수도 있다. 그러므로 온점을 붙이는것이 좋다. 잘못된 사용법에 관한 예시는 아래와 같다.<br><br>

    1) First item
    2) Second item

## Unordered Lists

순서가 없는 리스트를 만드는데 사용된다. `-`, `*`, `+` 이 셋 중 하나를 단락 앞에 입력하면서 순서 없는 리스트를 만들 수 있다. 예시는 다음과 같다.<br><br>

    - First item
    - Second item
    - Third item
    - Fourth item

    * First item
    * Second item
    * Third item
    * Fourth item

    + First item
    + Second item
    + Third item
    + Fourth item

->

- First item
- Second item
- Third item
- Fourth item

이 순서 없는 리스트도 순서 있는 리스트처럼 한 리스트 밑에 또다른 리스트를 만들 수 있다. 이 역시 `4번의 띄어쓰기`(`혹은 한 번의 탭`)를 이용해서 만들 수 있다. 예시는 다음과 같다. <br><br>

    - First item
    - Second item
    - Third item
        - Indented item
        - Indented item
    - Fourth item

->

- First item
- Second item
- Third item
  - Indented item
  - Indented item
- Fourth item<br><br>

주의해야 할 점은 세 가지 요소(`-`, `*`, `+`) 중 한 번에 한 가지 요소만 사용해야 한다는 것이다. 즉 하나의 리스트를 만드는데 3가지 요소를 혼합해서 쓰면 안된다는 것이다. 잘못된 사용법에 관한 예시는 다음과 같다.<br><br>

    + First item
    * Second item
    - Third item
    + Fourth item <br><br>

# Adding Elements in Lists

리스트에 달려있는 내용에 또다른 markdown language 요소들(단락 나누기, 인용 등)을 추가할 수 있다. *Code Blocks*을 제외한 어떤 요소들을 추가하든지 간에 반드시 해야할 것은 **특정 요소를 추가하려는 내용 맨 앞에 반드시 `4칸 띄어쓰기`(혹은 `1번의 탭`)를 하는 것** 이다. 다음과 같은 예시를 보면 더 잘 이해할 수 있을 것이다.<br><br>

## Paragraphs 만들기

    * This is the first list item.
    * Here's the second list item.

        I need to add another paragraph below the second list item

    * And here's the third list item.

->

- This is the first list item.
- Here's the second list item.

  I need to add another paragraph below the second list item.

- And here's the third list item.<br><br>

## Blockquotes 추가하기

    * This is the first list item.
    * Here's the second list item.

        > A blockquote would look great below the second list item.

    * And here's the third list item.

-> <br>

- This is the first list item.
- Here's the second list item.

  > A blockquote would look great below the second list item.

- And here's the third list item.

## Code Blocks 추가하기

리스트 내에 특정 코드를 블럭으로 감싸게 하는 기능이다. 이 기능을 이용하려면 블럭으로 감싸려는 코드마다 `8번의 띄어쓰기`(혹은 `2번의 탭`)을 입력해야 한다. 예시는 다음과 같다.<br><br>

    1. Open the file.
    2. Find the following code block on line 21:

            <html>
              <head>
                <title>Test</title>
              </head>

    3. Update the title to match the name of your website.

->

1.  Open the file.
2.  Find the following code block on line 21:

        <html>
          <head>
            <title>Test</title>
          </head>

3.  Update the title to match the name of your website.<br><br>

## Images 추가하기

이미지를 넣는 기능으로, 이미지를 넣는 자세한 방법은 아래 _Image_ 문단을 참고하면 된다.<br><br>

    1. Open the file containing the Linux mascot.
    2. Marvel at its beauty.

        ![Tux, the Linux mascot](https://s3.ap-northeast-2.amazonaws.com/opentutorials-user-file/course/94.png)

    3. Close the file.

-> <br>

1.  Open the file containing the Linux mascot.
2.  Marvel at its beauty.

    ![Tux, the Linux mascot](https://s3.ap-northeast-2.amazonaws.com/opentutorials-user-file/course/94.png)

3.  Close the file.

## Lists내에 또다른 Lists 넣기

순서 있는 리스트 안에 순서 없는 리스트를 넣을 수 있다. 그 반대도 가능하다. 예시는 다음과 같다. <br><br>

    1. First item
    2. Second item
    3. Third item
        - Indented item
        - Indented item
    4. Fourth item

-> <br>

1. First item
2. Second item
3. Third item
   - Indented item
   - Indented item
4. Fourth item<br><br>

# Code

어떤 문구나 단어를 '코드'로 표현하는 도구로, `` 백틱(`) ``을 해당 문구 혹은 단어 앞뒤로 추가하면서 표현할 수 있다 예시는 다음과 같다.<br><br>

    At the command prompt, type `nano`.

-> At the command prompt, type `nano`.<br><br>

만일 `` 백틱(`) `` 문자가 코드로서 들어가야 한다면, 코드로 표현하고자 하는 문장 앞뒤로 `` 백틱(`) ``을 2개를 연속으로 추가함으로서 표현할 수 있다. 예시는 다음과 같다.<br><br>

    ``Use `code` in your Markdown file.``

-> `` Use `code` in your Markdown file. ``<br><br>

## Code Block

코드를 블럭으로 감싸면서 표현하고 싶다면, 표현하고자 하는 문장 맨 앞에 최소 `4칸 띄어쓰기`(혹은 `1번의 탭`)를 함으로서 표현할 수 있다. 예시는 다음과 같다.<br><br>

    (스페이스)(스페이스)(스페이스)(스페이스)<html>
      (스페이스)(스페이스)(스페이스)(스페이스)<head>
      (스페이스)(스페이스)(스페이스)(스페이스)</head>
    (스페이스)(스페이스)(스페이스)(스페이스)</html>

->

    <html>
      <head>
      </head>
    </html>

<br><br>

# Horizontal Rules

내용을 구분하는 기준선을 만드는 기능으로 원하는 문장 밑에 실선을 만들어 준다. 원하는 문장 밑에 `*`, `_`, `-`을 최소 3번 이상(`***`, `______`, `----`) 입력해주면 된다. 유의해야 할 사항은 이 문자 위 아래로 최소 한 번 이상의 `(엔터)`가 입력되 있어야 한다. 엔터가 입력되있지 않으면 실선을 만들지 않고 해당 문자 위의 내용을 **제목**으로 만든다. 올바른 예시는 다음과 같다.<br><br>

    Try to put a blank line before...

    ---

    ...and after a horizontal rule.<

-><br>

Try to put a blank line before...

---

...and after a horizontal rule.<br><br>

잘못된 예시는 다음과 같다.<br><br>

    Without blank lines, this would be a heading.
    ---
    Don't do this!

-><br>

## Without blank lines, this would be a heading.

Don't do this!<br><br>

# Links

원하는 부분을 링크가 걸려있도록 만들 수 있는 기능이다. `[]`(대괄호) 안에 링크를 걸고 싶은 문구를 넣고, `[]` 바로 뒤에 `()`(소괄호) 안에 링크 주소를 넣으면 된다. 예시는 다음과 같다.<br><br>

    My favorite search engine is [Duck Duck Go](https://duckduckgo.com\).

-><br>

My favorite search engine is [Duck Duck Go](https://duckduckgo.com). <br><br>

## Adding Titles

링크에 마우스를 갖다 대었을때(클릭은 안하고) 내가 설정한 부가 설명이 뜨게 할 수 있는 기능이다. 링크 주소를 넣는 `()`(소괄호)안에서 링크 주소가 끝나는 지점에 추가하고자 하는 내용을 `""`(큰따옴표)로 감싸면 된다. 예시는 다음과 같다.<br><br>

    My favorite search engine is [Duck Duck Go](https://duckduckgo.com "The best search engine for privacy").

-> <br>

My favorite search engine is [Duck Duck Go](https://duckduckgo.com "The best search engine for privacy").

마우스를 갖다 대면 "The best search engine for privacy"가 뜨는 것을 확인할 수 있다.<br><br>

## URLs and Email Addresses

빠르게 링크 주소나 이메일 주소를 원하는 문구에 걸고 싶다면, `<>`(각진 괄호)로 그 문구를 감싸면 된다. 예시는 다음과 같다.<br><br>

    <https://www.markdownguide.org>
    <fake@example.com>

-> <br>

<https://www.markdownguide.org>  
<fake@example.com> <br><br>

## Formatting Links

링크가 걸려있는 문구 역시 강조(글씨 굵게하기, 글꼴 기울이기)와 코드로 표현하기가 가능하다. 링크화시킨(이미 명령어가 붙여진) 해당 내용 맨 앞과 맨 뒤에 사용하고자 하는 명령어를 붙이면 된다. 예시는 다음과 같다.<br><br>

    I love supporting the **[EFF](https://eff.org)*_.
    This is the *[Markdown Guide](https://www.markdownguide.org)_.
    See the section on [`code`](https://www.markdownguide.org).

->

I love supporting the **[EFF](https://eff.org)**.  
This is the _[Markdown Guide](https://www.markdownguide.org)_.  
See the section on [`code`](https://www.markdownguide.org).
<br><br>

## Reference-style Links

참조 링크라고 하는데, 링크를 id값을 통해서 걸려는 것이다. 이 말은 즉슨, 링크에 id값을 미리 지정해놓고 어떤 문구에 링크를 걸려고 할 때, 위에서 언급한 문법을 사용해서가 아니라 미리 설정해둔 id값을 이용해서만 링크를 거는 것이다.<br>

id값 설정은 원하는 주소를 적은 다음 그 주소 맨 앞부분에 `[]`(대괄호)로 감싸져있는 id값을 대입하면 된다. 그리고 그 id를 이용할 때에는 링크를 걸고자 하는 문구를 `[]`(대괄호)로 감싸고 바로 뒤에(띄어쓰기 하면 안된다.) `[]`(대괄호)로 감싸져있는 id값을 추가함으로서 링크를 걸 수 있다. 예시는 다음과 같다.<br><br>

    [1]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> "Hobbit lifestyles"

    [Hobbit][1]

-> <br>

[1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles"

[Hobbit][1]<br><br>

링크를 걸 때 유의해야 할 사항이 있다. 링크에 `공백`이 들어가있으면 안된다는 것이다. 만약 링크에 공백이 들어가 있다면 공백을 지우고 공백 한 칸당 `%20`으로 채워넣자.,<br><br>

# Images

문서에 이미지를 추가하는 기능이다. 우선 이미지의 이름(마우스를 갖다 댔을때 뜨는 문구)를 `[]`(대괄호)로 묶는다. 그리고 `[]` 바로 앞에는 `!`를 붙인다. 또한 `[]` 바로 뒤에는 `()`(소괄호)를 추가하고 그 소괄호 안에 해당 이미지의 링크(혹은 해당 이미지의 경로)를 추가하면 된다. 예시는 다음과 같다.<br><br>

    ![생활코딩!!!](https://s3.ap-northeast-2.amazonaws.com/opentutorials-user-file/course/94.png)

-> <br>

![생활코딩!!!](https://s3.ap-northeast-2.amazonaws.com/opentutorials-user-file/course/94.png)<br><br>

또한 이미지에 링크를 달 수 있다. 링크를 달 때는 원래 이미지를 추가하는 방식대로 명령어를 입력하고 그 사이를 `[]`(대괄호)로 감싸준다. 그리고 감싸진 대괄호 바로 뒤에 `()`(소괄호)를 붙이고 그 소괄호 안에 원하는 링크를 넣으면 된다. 예시는 다음과 같다.<br><br>

    [![생활코딩!!!](https://s3.ap-northeast-2.amazonaws.com/opentutorials-user-file/course/94.png)](https://opentutorials.org/course/1)

->

[![생활코딩!!!](https://s3.ap-northeast-2.amazonaws.com/opentutorials-user-file/course/94.png)](https://opentutorials.org/course/1)<br><br>

# Escaping Characters

`*`나 `<>`같은 리터럴 문자들을 명령어로 쓰지 않고 Markdown 문서 안에 단지 표현하기 위해서 쓰고 싶을 때가 있을 것이다. 그럴 때는 해당 명령어 바로 앞에 백슬래쉬(`\`)를 붙이면 된다. 예시는 다음과 같다.<br><br>

    \* Without the backslash, this would be a bullet in an unordered list.

-> <br>

\* Without the backslash, this would be a bullet in an unordered list.<br><br>

아래는 Escape 할 수 있는 명령어들을 표로 만든 것이다.<br><br>

| Character | Name                                           |
| --------- | ---------------------------------------------- |
| \\        | backslash                                      |
| \`        | backtick (see also escaping backticks in code) |
| \*        | asterisk                                       |
| \_        | underscore                                     |
| \{ }      | curly braces                                   |
| \[ ]      | brackets                                       |
| \< >      | angle brackets                                 |
| \( )      | parentheses                                    |
| \#        | pound sign                                     |
| \+        | plus sign                                      |
| \-        | minus sign (hyphen)                            |
| \.        | dot                                            |
| \!        | exclamation mark                               |
| \|        | pipe (see also escaping pipe in tables)        |

<br><br>

# HTML

Markdown문서 안에서 HTML 태그가 사용 가능하다. 글자를 기울이는 태그가 \<em>이라고 할 떄, 다음과 같이 글자를 기울이게 할 수 있다.<br><br>

    This <em>word</em> is italic.

-> <br>

This <em>word</em> is italic.<br><br>

하지만 모든 Markdown 어플리케이션이 모든 HTML태그를 사용할 수 있게 허용하지는 않는다. 일부 어플리케이션에서는 HTML 태그 중 일부만 쓸 수 있도록 허용해 놓았다. 그러므로 HTML 태그를 쓴다면 반드시 md파일을 열어봐서 제대로 적용이 됬는지 확인해봐야한다.
추가로 HTML 태그 안에서 Markdown 언어는 사용할 수 없다.

<https://github.com/codejoo9098/Code_JJW>
