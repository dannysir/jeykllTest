---
title: Programmers 코딩테스트 (8)
tags: [Programmers, Coding Test]
style: fill
color: light
description: programmers - 정수 내림차순으로 배치하기 - 문제 풀이
---

# 2022-11-30 TIL

## programmers

### 정수 내림차순으로 배치하기

### 문제설명

---

함수 solution은 정수 n을 매개변수로 입력받습니다. n의 각 자릿수를 큰것부터 작은 순으로 정렬한 새로운 정수를 리턴해주세요. 예를들어 n이 118372면 873211을 리턴하면 됩니다.

### 제한사항

---

- `n`은 1이상 8000000000 이하인 자연수입니다.

### 입출력 예

---

| n      | return |
| ------ | ------ |
| 118372 | 873211 |

### 풀이

---

```jsx
function solution(n) {
  var answer = 0;
  //n 값을 String으로
  let nString = String(n);
  //split으로 배열을 나누어주고 sort()를 이용해서 내림차순 정렬
  const sanArr = nString.split("").sort((a, b) => {
    return b - a;
  });
  //join 을 이용하여 배열을 String으로 합쳐줌
  const newArr = sanArr.join("");
  answer = parseInt(newArr);
  return answer;
}
```
