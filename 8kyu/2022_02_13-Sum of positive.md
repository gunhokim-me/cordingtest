## Isograms
https://www.codewars.com/kata/5715eaedb436cf5606000381

### 문제
You get an array of numbers, return the sum of all of the positives ones.
Note: if there is nothing to sum, the sum is default to 0.

Examples
```
[1,-4,7,12] --> 1 + 7 + 12 = 20
```

### 풀이
#### 작성한 코드
```java
int result = 0;
for(int sum : arr) {
  if(sum > 0) {
    result += sum;
  }
}
return result;
```

1. 배열에 있는 값을 양수인지 한개 씩 체크한다.
2. 양수인 경우에 result 변수에 값을 더한다.

### Clever Code
```java
return Arrays.stream(arr).filter(v -> v > 0).sum();
```
1. 스트림을 통해 배열을 자동으로 꺼낸다.
2. 필터 메서드에서 스트림 내부 값을 체크 하고 양수인 경우에 값을 더하도록 한다.

java.util.Arrays 를 import 시켜줘야 코드가 작동한다.
