## Isograms
https://www.codewars.com/kata/51f2d1cafc9c0f745c00037d/java

### 문제
Complete the solution so that it returns true if the first argument(string) passed in ends with the 2nd argument (also a string).

Examples
```
solution('abc', 'bc') // returns true
solution('abc', 'd') // returns false
```

### 풀이
#### 작성한 코드
```java
return str.endsWith(ending);
```

1. 주어진 문자열의 마지막 문자와 비교하는 문자열과 같으면 true, 아니면 false를 반환한다.

### Clever Code
위에 작성한 코드와 동일.

### 총평
startWith, endswith을 알고 있었기에 쉽게 풀수 있는 문제였다.
