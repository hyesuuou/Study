2020.12.25

커밋은 **작은 단계로 커밋**하여 코드 개발 과정을 가시적으로 보여주어야 한다. 한꺼번에 모든 파일과 코드를 커밋하는 것은 잘못된 습관 중 하나다. 메서드 리팩터링이나 새로운 메서드나 클래스를 추가할 때, 혹은 실험이나 성능 튜닝을 할 때에도 각 단계별로 커밋한다. 소스 코드 변경 내역이 없을 경우에는 커밋하지 않는다.

## 커밋 메시지는 **제목, 본문(선택), 꼬리말(선택)** 세 부분으로 나눠진다.

```
type: subject

body

footer
```

### Commit Type

- feat - 새로운 기능 추가
- fix - 버그 수정
- docs - 문서 수정
- style - 코드 포맷팅, 세미콜론 누락, 코드 변경이 없는 경우
- refactor - 코드 리팩토링
- test - 테스트 코드, 리팩토링 테스트 코드 추가
- chore - 빌드 업무 수정, 패키지 매니저 수정

### Subject

- 제목은 50자를 넘기지 않는다.
- 대문자로 시작한다.
- 마침표를 붙이지 않는다.
- 과거시제를 사용하지 않고, 명령어로 작성한다.

    깃은 커밋메시지의 기본값으로 명령문을 사용한다. 따라서 제목을 명령문으로 작성하는 것은 git의 Built-in Convention을 그대로 따르는 것이며, 자동으로 채워진 커밋 사이에 자연스럽게 녹아들 수 있다. (물론 본문은 평서문으로 작성해야 한다. 여기서는 제목을 작성하는 경우만 해당한다.)

    명령문으로 작성하는 것이 혼란스럽다면, 'If applied, this commit will ~' 뒤에 들어갈 말을 생각해 보자.  ex) (If applied, this commit will) **Remove deprecated methods.**

### Body

- 선택사항이므로 모든 커밋에 작성할 필요는 없으며, 부연설명이 필요하거나 커밋의 이유를 설명할 경우 작성한다.
- 72자마다 줄을 바꾼다.
- 어떻게 보다는 **"무엇을", "왜"**에 초점을 맞추어 작성한다.
- 제목과의 구분을 위해 한 칸을 띄운 후 작성한다.

### footer

- 선택사항이므로 모든 커밋에 꼬리말을 작성할 필요는 없다.
- issue tracker id 를 작성할 때 사용한다.

### 많이 쓰는 커밋 명령어 정리
- Fix  - 보통 올바르지 않은 동작을 고친 경우에 사용한다.
- Add - 코드나 테스트, 예제, 문서 등의 추가가 있을 때 사용한다.
- Remove - 코드의 삭제가 있을 때 사용한다.
- Refactor - 전면 수정이 있을 때 사용한다.
- Update - 원래도 정상적으로 동작하고 있었으나 수정, 추가, 보완 한다는 개념이다. 코드보다는 주로 문서나 리소스, 라이브러리 등에 사용한다.
- Improve - 향상이 있을 때 사용한다.(호환성, 테스트 커버리지, 성능, 검증 기능, 접근성 등 다양한 것들 목적)
- Make - 주로 기존 동작의 변경을 명시한다.
- Revise - 문서의 개정이 있을 때 주로 사용한다.
- Correct - 주로 문법의 오류나 타입의 변경, 이름 변경 등에 사용한다.
- Move - 코드의 이동이 있을 때 사용한다.
- Rename - 이름 변경이 있을 때 사용한다.
- Verify - 검증 코드를 넣을 때 주로 사용한다.
- Set - 변수 값을 변경하는 등의 작은 수정에 주로 사용한다.


---
> 참고

[https://velog.io/@hyeong412/TIL-좋은-커밋-메세지-작성하기-](https://velog.io/@hyeong412/TIL-%EC%A2%8B%EC%9D%80-%EC%BB%A4%EB%B0%8B-%EB%A9%94%EC%84%B8%EC%A7%80-%EC%9E%91%EC%84%B1%ED%95%98%EA%B8%B0-)

[https://sujinlee.me/professional-github/](https://sujinlee.me/professional-github/)

[https://rok93.tistory.com/entry/Git-Commit-Message-Convention](https://rok93.tistory.com/entry/Git-Commit-Message-Convention)
