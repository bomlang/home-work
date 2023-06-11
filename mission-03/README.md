# webCafe 사이트 일부 구현

## 트리 구조

```
body
  section
    article
      h2
      div.event-relate__container
        div.event__container
          h3.event__title
          (content)

        div.relate__container
          h3.relate__title
            span*2
          div.relate__listBox
            ul .relaate__listBox__site
              li
                a
              (content)
```

---

## 🤔 코드 조건

> **과제 조건**
>
> 1. 관련 사이트는 제목으로 각각 항목은 링크로 구현한다.
> 2. 링크 목록은 5개이며 CSS를 사용하여 화면에 1개의 목록만 보이도록 구현한다.
> 3. 목록에 마우스를 올리면 5개의 목록이 펼쳐지도록 구현한다.
> 4. transition 속성을 활용하여 애니메이션 효과를 적용한다.

- li태그 안쪽에 a태그를 쓰고 `text-decoration: none;`, `color: black;` 을 추가하여 링크의 고유속성을 지웠다.
- figma에 주어진 박스의 크기대로 설정하면 링크가 5개가 나와서 임의로 박스크기를 링크가 화면에 1개만 보이도록 사이즈를 조절하였다. 박스에 마우스를 올릴시 5개가 모두 보이도록 구현해보았다.
- 목록에 마우스를 올리면 5개의 목록이 펼쳐지면서 figma에 주어진 값대로 박스가 크기를 가진다.
- `transition`속성을 사용하여 `event-relate__contain`e에 마우스를 올릴시 `relate__list`에 존재하는 5개의 list가 보여진다.

---

## 과제 하면서 느낀점

- 욕심으로 과제범위를 벗어나 박스하나를 다 만들었다.

  - `hover`를 이용하여 height값을 설정했고, `transition`으로 `height`값이 변경될 때 조건을 걸어 움직이게 하였다. 이때 `hover`값을 `relate__box`에만 설정하고 싶었는데 문제가 있었다.

    - `relate__box`에 `hover`값을 설정하고 hover가 동작할때 `event-relate__listBox`가 움직이게 하려했지만, event-relate**list박스는 relate**box의 상위요소이기에 동작하지 않는다. 그래서 동작하게 하려면 ssas를 이용하여 if문을 이용하거나 JS를 이용하여 동작하는 방법밖에 없었다.

  - 처음엔 @keyframe과 scale을 써서 제작해보고 싶었는데 지식이 부족해 hover를 쓰는 방법이 최선이었다. 다양한 방법을 쓸 수 있도록 다음에는 hover가 아닌 다른 방법으로 코드를 써봐야겠다.

- 코드에 div가 너무 남발되는 느낌이 있다. 좀 더 간결하게 짜도록 노력해야겠다.
  - div가 많아지니까 class명도 길어지고 이름 짓기도 어려웠다.
