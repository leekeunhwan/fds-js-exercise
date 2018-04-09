### 문제 1

두 수를 입력받아 큰 수를 반환하는 함수를 작성하세요.

---

```javascript
function bigger(min, max) {
  if (min < max) {
    console.log(`큰 수는 ${max}입니다.`);
  } else {
    console.log(`큰 수는 ${min}입니다.`);
  }
}

bigger(233, 552);
```

```js
function larger(x, y) {
  return Math.max(x, y);
}
```

```js
function larger(x, y) {
  return x > y ? x : y;
}
```

<br/><br/>

### 문제 2

세 수를 입력받아 그 곱이 양수이면 `true`, 0 혹은 음수이면 `false`, 둘 다 아니면 에러를 발생시키는 함수를 작성하세요.

에러를 발생시키는 코드는 다음과 같습니다.

```js
throw new Error("입력값이 잘못되었습니다.");
```

---

```javascript
function test(a, b, c) {
  if (a * b * c > 0) {
    console.log(`true`);
  } else if (a * b * c < 0) {
    console.log(`false`);
  } else {
    throw new Error(`입력값이 잘못되었습니다.`);
  }
}

test(100, 200, 300);
test(100, -200, 300);
test(100, 0, 300);
```

```js
//보다 좋은 예

function isPositive(a, b, c) {
  const multi = a * b * c;
  if (multi > 0) {
    return true;
  } else if (multi <= 0) {
    return flase;
  } else {
    throw new Error("...");
  }
}

isPositive(100, 200, NaN);
```

<br/><br/>

### 문제 3

세 수 `min`, `max`, `input`을 입력받아, 다음과 같이 동작하는 함수를 작성하세요.

* `min`보다 `input`이 작으면, `min`을 반환합니다.
* `max`보다 `input`이 크면, `max`를 반환합니다.
* 아니면 `input`을 반환합니다.

예:

```javascript
limit(3, 7, 5); -> 5
limit(3, 7, 11); -> 7
limit(3, 7, 0); -> 3
```

---

```js
function num3(min, max, input) {
  if (min > input) {
    return min;
  } else if (max < input) {
    return max;
  } else {
    return input;
  }
}

num3(3, 7, 10);
```

```js
function limit(min, max, input) {
  switch (true) {
    case min > input:
      console.log(min);
      break;
    case max < input:
      console.log(max);
      break;
    default:
      return input;
  }
}

limit(3, 7, 5);
```

<br/><br/>

### 문제 4

어떤 정수가 짝수인지 홀수인지 출력하는 함수를 작성하세요. 이를 이용해서, 1 부터 20 까지의 수가 각각 짝수인지 홀수인지 출력하는 프로그램을 작성하세요.

---

```js
function printEvenOrOdd() {
  for (i = 1; i <= 20; i++) {
    if (i % 2 === 0) {
      console.log(i + "는 짝수입니다.");
    } else {
      console.log(i + "는 홀수입니다.");
    }
  }
}

printEvenOrOdd();
```

<br/><br/>

### 문제 5

100 이하의 자연수 중 3 과 5 의 공배수를 모두 출력하는 프로그램을 작성하세요.

---

```js
function gongbae() {
  for (i = 1; i <= 100; i++) {
    if (i % 3 === 0 && i % 5 === 0) {
      console.log(`100이하의 자연수중 3과 5의 공배수는 ${i}입니다.`);
    }
  }
}

gongbae();
```

<br/><br/>

### 문제 6

자연수를 입력받아, 그 수의 모든 약수를 출력하는 함수를 작성하세요.

---

```js
function yaksu(num) {
  for (i = 1; i <= num; i++) {
    if (num % i === 0) {
      console.log(`${num}의 약수는 ${i}입니다.`);
    }
  }
}

yaksu(15);
```

<br/><br/>

### 문제 7

2 이상의 자연수를 입력받아, 그 수가 소수인지 아닌지를 판별하는 함수를 작성하세요.

---

### 문제 8

1 부터 100 까지의 수를 차례대로 출력하되, 자릿수에 3, 6, 9 중 하나라도 포함되어 있으면 '짝!'을 대신 출력하는 프로그램을 작성하세요.

### 문제 9

양의 정수를 입력받아, 다음과 같은 패턴의 출력을 하는 함수를 작성하세요.

1 을 입력받은 경우:

```
*
```

3 을 입력받은 경우:

```
*
* *
* * *
```

5 를 입력받은 경우:

```
*
* *
* * *
* * * *
* * * * *
```

### 문제 10

양의 정수를 입력받아, 다음과 같은 패턴의 출력을 하는 함수를 작성하세요.

1 를 입력받은 경우:

```
*
```

3 를 입력받은 경우:

```
  *
 * *
* * *
 * *
  *
```

5 를 입력받은 경우:

```
    *
   * *
  * * *
 * * * *
* * * * *
 * * * *
  * * *
   * *
    *
```

### 문제 11

두 수를 입력받아서, 두 수의 최대공약수를 반환하는 함수를 작성하세요. ([유클리드 호제법](https://ko.wikipedia.org/wiki/%EC%9C%A0%ED%81%B4%EB%A6%AC%EB%93%9C_%ED%98%B8%EC%A0%9C%EB%B2%95)을 참고하세요.)

### 문제 12

세 수를 입력받아 큰 것부터 차례대로 출력하는 함수를 작성하세요.

### 문제 13

자연수 `n`을 입력받아, `n`번째 피보나치 수를 반환하는 함수를 작성하세요.
