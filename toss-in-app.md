---
title: 토스 인 앱 반려 사유 'eval'
category: App
---

써드파티의 JavaScript 라이브러리를 쓰다보면, 클린 코드를 학습하고 객체 지향 코드를 작성하다 보면, 보안 공부를 하다보면 자주 마주치는 함수가 있다.
> eval()
String 으로 작성된 것을 마음대로 타입 변환해서 반환하게끔 해주는 함수다.
왜 문제가 될까? [CTF 예시](https://github.com/Parveshdhull/CTF-Writeups/blob/master/2021/TetCTF%202021/Super%20Calc.md) 뿐만 아니라 권한 문제를 탈취할 수도 있으므로 아예 안 쓰는 것이 맞다.
그렇다면 해결 방법은? 써드파티의 eval 관련 함수를 false로 설정한다. 또는 해당 라이브러리를 사용하지 않는다.