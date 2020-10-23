---
title: 
author: Chanyoung Lee
date: 2020-10-22 11:33:00 +0800
categories: [큰 범주, 작은 범주]
tags: []
math: true
image: 
---

```
prompt("당신의 나이는?"); 
```
위의 코드는 창이 뜨게 해서 밑의 이미지가 뜨게 한다

![prompt](/assets/img/Javascript/prompt.png)


## 기타 false로 간주되는 데이터형
``` javascript
if('') {
    alert(1);
}
  
if (undefined) {
    alert('undefined');
}

if (null) {
    alert('null');
}
if(!NAN) {
    alert('NaN');
}
이럴 경우 false라서 실행이 되지 않는다. 
```

## 함수의 또 다른 정의
```javascript
numbering = function() {
    var a = 3;
}

function numbering() {
    var a = 3;
}

위의 두 개는 동일
```
## 익명함수
```javascript
(function() {
    var i = 3;
    return i;
})() //익명함수, 바로 실행시켜준다.
```