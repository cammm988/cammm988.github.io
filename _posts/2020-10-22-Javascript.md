---
title: 
author: Chanyoung Lee
date: yyyy-mm-dd 11:33:00 +0800
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
