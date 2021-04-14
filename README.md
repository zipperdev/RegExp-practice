# 정규표현식(RegExp)

#### 정규식이라 줄여 부르기도 하고
#### RegExp는 Regular Expression의 줄인것이다

---
<br />

## 역할

* 문자 검색(search)
* 문자 대체(replace)
* 문자 추출(extract)
<br />
<br />

## 테스트 사이트

[정규식 테스트 해보기(https://regexr.com)](https://regexr.com/)
<br />
<br />

## 정규식 생성

```js
// 생성자
new RegExp("표현", "옵션");
new RegExp("[a-z]", "gi");

// 리터럴
/표현/옵션
/[a-z]/gi
```
<br />
<br />

## 예제 변수

```js
const str = `
010-1234-5678
zipper@zipperdev.com
https://www.omdbapi.com
The quick brown fox jumps over the lazy dog.
abbcccdddd
`;
```
<br />
<br />

## 메소드

메소드 | 문법 | 설명
--|--|--
test | `정규식.test(문자열)` | 일치 여부(Boolean) 반환
match | `문자열.match(정규식)` | 일치하는 문자의 배열(Array) 반환
replace | `문자열.replace(정규식, 대체문자)` | 일치하는 문자를 대체
<br /><br />


## 플래그(옵션)

플래그 | 설명
--|--
g | 모든 문자 일치(global)
i | 영어 대소문자를 구분하지 않고 일치(ignore case)
m | 여러 줄 일치(multi line)

## 패턴(표현)

패턴 | 설명
--|--
^ab | 줄(Line) 시작에 있는 ab와 일치
ab$ | 줄(Line) 끝에 있는 ab와 일치
. | 임의의 한 문자와 알치
a&verbar;b | a 또는 b와 일치
ab? | b가 없거나 b와 일치
{3} | 3개 연속 일치
{3,} | 3개 이상 연속 일치
{3,5} | 3개 이상 5개 이하(3~5개) 연속 일치
[abc] | a 또는 b 또는 c
[a-z] | a부터 z 사이의 문자 구간에 일치(영어 소문자)
[A-Z] | A부터 Z 사이의 문자 구간에 일치(영어 대문자)
[0-9] | 0부터 9 사이의 문자 구간에 일치(숫자)
[가-힣] | 가부터 힣 사이의 문자 구간에 일치(한글)
\w | 63개 문자(Word, 대소영문52개 + 숫자10개 + _)에 일치
\b | 63개 문자에 일치하지 않는 문자 경계(Boundary, \w에 포함되지 않는 것 일치)
\d | 숫자(Digit)에 일치
\s | 공백(Space, Tab 등)에 일치
(?=) | 앞쪽 일치(Lookahead)
(?<=) | 뒤쪽 일치(Lookbehind)