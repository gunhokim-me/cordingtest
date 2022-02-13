## Vowel Count
https://www.codewars.com/kata/54ff3102c1bad923760001f3/javascript

### 문제
Return the number (count) of vowels in the given string.
We will consider a, e, i, o, u as vowels for this Kata (but not y).
The input string will only consist of lower case letters and/or spaces.

Examples
```
"abracadabra" --> 5
"pear tree"   --> 4
"my pyx"      --> 0
```

### 풀이
#### 작성한 코드
```javascript
function getCount(str) {
  var vowelsCount = 0;
  
  // enter your majic here
  var splitStr = str.split('');
  for(var index = 0; index < splitStr.length; index++) {
    if(splitStr[index] == 'a' || splitStr[index] == 'e' || splitStr[index] == 'i' || splitStr[index] == 'o' || splitStr[index] =='u') {
      vowelsCount++;
    }
  }
  return vowelsCount;
}
```

1. 주어진 문자열을 한개씩 나누어 배열에 담는다.
2. 소문자 a,e,i,o,u 가 주어지는 문자열에 있는지 확인하면 되기 때문에 배열에서 한개씩 확인 한다.
3. 배열 속 문자열과 a,e,i,o,u 문자열 중 하나가 같으면 vowelsCount 값을 증가시킨다.

### Clever Code
```javascript
function getCount(str) {
  return (str.match(/[aeiou]/ig)||[]).length;
}
```
정규표현식 해석 : /[aeiou]/ig
 - [] : 괄호안의 문자들 중 하나
 - i  : Ignore Case -> 대소문자 구분 안함
 - g  : Global -> 모든 문자 검색 (이거 없으면 매칭되는 첫 문자만 검색 하고 끝)


### 총평
7급 자바스크립트 문제인제 매우 쉽다.
정규표현식으로 하면 더욱 쉽게 풀수있는 것을 보니 정규표현식을 공부 해야할 듯 하다.
