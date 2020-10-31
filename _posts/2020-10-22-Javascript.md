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
//이럴 경우 false라서 실행이 되지 않는다. 
```

## 함수의 또 다른 정의
```javascript
numbering = function() {
    var a = 3;
}

function numbering() {
    var a = 3;
}
//위의 두 개는 동일
```
## 익명함수
```javascript
(function() {
    var i = 3;
    return i;
})() //익명함수, 바로 실행시켜준다.
```

## 다양한 함수 (배열관련)

```javascript
splice() // 몇 번째에 몇 개를 제거하고 명시된 원소 추가
unshift() // 배열 맨 앞에 추가
shift() // 첫 번째 원소 제거
push() // 원소 맨 뒤에 추가
pop() // 원소 맨 뒤 보고 꺼내기 
sort() // 정렬
reverse() //거꾸로 하기  
```

## 객체의 생성

```javascript
var box = {'egoing' : 10, 'dgoing' : 5, 'cgoing' : 30};
console.log(box['egoing']) // 호출방법 1 
console.log(box.egoing) // 호출방법 2
console.log(box['eg'+'oing']) // 호출방법 3

var a = {'a' : 20, 'b': 30};
    for (var name in a) {
        document.write(`<li> ${name} is ${a[name]} </li>`); } 
//object 활용 방법
```

## 객체 지향 프로그래밍

```javascript
var grades = {'list' : {'egoing' : 10, 'k8805' : 8, 'sorialgi' : 80}, 
'show' : function() {
    alert('hello world');
    }   } // 함수를 object로 이용
alert(grades['list']); // {egoing: 10, k8805: 8, sorialgi: 80}
alert(grades['show']()); // alert가 뜸.(hello world)

var grades = {'list' : {'egoing' : 10, 'k8805' : 8, 'sorialgi' : 80}, 
'show' : function() {
    alert(this.list); //함수가 속해 있는 객체를 가리키는 변수.  
    }   } // 함수를 object로 이용
```

## 모듈화
```javascript
<script src = "greeting.js"> 
</script> //greeting.js 파일을 찾아봄
```

## 값으로서의 함수
```javascript
a = {
    b: function() {
        // 객체 안에 저장된 함수
    }
}
//함수를 이용하여 인자로 전달
function cal(func, num) {
    return func(num);
}
function increase(num) {
    return num+1;
}
alert(cal(increase, 1));
```
## 함수 return 하기
```javascript
function cal(mode){
    var funcs = {
        'plus' : function(left, right){return left + right},
        'minus' : function(left, right){return left - right}
    }
    return funcs[mode];
}
alert(cal('plus')(2,1));
alert(cal('minus')(2,1));   
```

## 함수의 속성 정하기
```javascript
function factory(title) {
        return {
            get_title : function () {
                return title;
            },
            set_title : function(_title) {
                title = _title;
            }
        }
    }
    ghost = factory('Ghost in the shell');
    matrix = factory('Matrix');
```
오류문제
```
 var arr = []
    for(var i = 0; i < 5; i++){
        arr[i] = function(){
            return i;
        }
    }
    for(var index in arr) {
        console.log(arr[index]());
    }
//결과는 5가 다섯개 나온다.
```

## 함수 호출
```javascript


```