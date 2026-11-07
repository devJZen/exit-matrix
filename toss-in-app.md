---
title: 토스 인 앱 반려 사유 'eval'
category: App
---

써드파티의 JavaScript 라이브러리를 쓰다보면, 클린 코드를 학습하고 객체 지향 코드를 작성하다 보면, 보안 공부를 하다보면 자주 마주치는 함수가 있다.
코드는 누가봐도 간결하고 엘레강스하길 바라는 신입을 충격 받게 하는 함수 [eval](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/eval)은 그 어떤 레거시보다 세대갈등을 일으키기 충분했다.
입사 했는데 eval로 작성된 코드, 컨벤션이 존재 하지 않는 프로젝트, 온보딩이 전혀 되지 않는 회사? 생각보다 많을 것이다. 이런 상황에서 어떻게 연장자 또는 선배의 심기를 거스르지 않고 eval을 없애고 안전하고 새로 패치된 함수를 서빙할 수 있을까?

> eval()

String 으로 작성된 것을 마음대로 타입 변환해서 반환하게끔 해주는 함수다.
왜 문제가 될까? [CTF 예시](https://github.com/Parveshdhull/CTF-Writeups/blob/master/2021/TetCTF%202021/Super%20Calc.md) 뿐만 아니라 권한 문제를 탈취할 수도 있으므로 아예 안 쓰는 것이 맞다.
어쩔 수 없어서 작성된 경우? [pdf.js](https://github.com/mozilla/pdf.js/issues/16061) 어쩔 수 없다고 하긴 하지만 대안은 항상 있으니 확인한다.
그렇다면 반려 해결 방법은? 써드파티의 eval 관련 함수를 false로 설정한다. 또는 해당 라이브러리를 사용하지 않는다.