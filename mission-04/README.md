# webCafe 사이트 일부 구현

## 트리 구조

```
section#news__container
  div.news
    h2.news__title
      div.news__nav
        a(#)
          img
          span
  div.horizon
  div.news__main
    a(www.w3.org).news__main__img
      figure#news__img
        img
        figcaption
    div.news__main__title
      strong
      span
    p
    (content)
```

---

## 🤔 코드 조건

> **과제 조건**
>
> 1. grid 실습을 위한 과제 파일은 mission-04/grid.html 파일과 mission-04/grid.css 파일을 생성 후 각각 마크업과 스타일을 작성한다.
> 2. 더보기 링크 앞에 플러스 기호는 생략해도 무방하다. 3.이미지는 “W3C 리뉴얼”이라는 캡션 위에 썸네일 이미지를 사용한다. (해당 이미지는 배경으로 지정하지 말고 <img> 요소를 사용하여 콘텐츠 이미지로 배치)
> 3. grid를 활용하여 레이아웃을 구현한다.
> 4. mission-04/README.md 파일을 생성한 후 마크업 코드와 CSS 코드에 대한 설명을 적고 아래 이미지와 같이 완성된 UI 스크린샷을 삽입한다.

- 먼저 `section`태그를 컨테이너로 잡고 안에 `div` 를 3개로 나눠 `header` 영역과 `horizon` 수평선 영역, `main`컨텐츠 영역으로 나눴습니다.

- 메인 헤더쪽엔 '새소식'이라는 글이 있어 heading 으로 지정하고 더보기는 아이콘대신 이미지를 삽입하여 anchor 태그로 묶고, `flex를 사용`하여 header를 양쪽 끝으로 정렬하였습니다.

- header에 a태그에 이미지와 span태그를 정렬하기 힘들어 flex를 이용하여 해결하였습니다.

  - 이 부분은 float이나 position을 사용해봐도 좋을 것 같습니다.

- horizon 영역은 height값을 1px을 지정하여 linear-gradient를 적용하였고, section에 relative를 주고 horizon에 absolute를 주어 이동하게 했습니다.

- 오늘으 메인 과제인 grid는 main영역을 horizon 아래쪽에 배치하여 3 / 3으로 영역을 나눠 지정해보았습니다.

  - repeat값을 height값에 1fr을 주게되면 아래쪽으로 크게 늘어나 54px이라는 지정된 값을 할당해 크기를 정했습니다.

- 나머지 img부분은 figure안에 flex를주어 figcaption과 img를 중앙에 배치하고 margin을 주어 main중앙에 여백을 주었습니다.

---

## ✅ 과제 하면서 느낀점

- grid 영역을 지정할 때 row쪽에 1fr을 주게되면 하단쪽이 엄청나게 늘어나는 이슈가 있어 크기를 지정해서 사용하였습니다. 아직 grid를 이해하지 못했다고 파악하여 이번 주말 grid를 좀 더 공부하고 layout을 하나 코딩해 볼 생각입니다.

- 아직 마크업 단계에서 flex를 자주 사용하다보니 grid를 사용한다는 가정하에 마크업하려니 뇌정지가 와버렸습니다. 이 부분또한 마크업을 꾸준히 익혀야 할 것 같습니다.

- news\_\_header영역에 더보기박스에 이미지와 span을 맞추는데 flex부터 사용해서 과도한 코딩을 한거같습니다. 좀 더 간편한 방법이 있는지 찾아봐야겠습니다.

---

## 완성본

![과제 완성 이미지](img/grid.png "완성본 이미지")
