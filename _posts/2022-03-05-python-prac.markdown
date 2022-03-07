---
layout: post
title: 1일차. Python 기초
image: python.png
date: 2022-03-05 15:35:20 +0200
tags: [python]
categories: python
---

## 파이썬 프로그램에서 문장(Statement)
파이썬 프로그램을 구성하는 기본 단위이며 컴퓨터에게 작업을 지시하는 단위이다. <br>
파이썬 프로그램에서는 한 줄이 문장 하나가 되며 문장 단위로 순차적으로 실행이 된다.
<hr>

## 키워드(Keyword: 예약어)
파이썬에서 미리 정의된 단어
<hr>

## 식별자(Identifier)
변수명(variable name)과 함수명(function name)을 말함.

<hr>

## 들여쓰기(Indent)
같은 단계에 있는 문장들은 반드시 같은 들여쓰기를 해야하며
같은 들여쓰기를 사용하는 문장들의 집합을 블록(Block)이라고 함.
<hr>

## 산술 연산자
산술 연산자로는 +(덧셈), -(뺄셈), *(곱셈), /(나눗셈), //(나눗셈), %(나머지), **(거듭제곱) 으로 구성된다.  
여기서 나눗셈 /와 //는 차이가 있다.
* 나눗셈 / : 실수로 표현
* 나눗셈 // : 정수로 표현(몪만 나온다.)<br>
{% highlight python %}
print('나눗셈 5 / 2 =', 5 / 2)
print('나눗셈 5 // 2 =', 5 // 2)

{% endhighlight %}
<br>
![]({{site.baseurl}}/images/python/20220305-1.png)

<hr>
## 대입 구문
변수에 참조할 값을 설정하는 구문이며 우변에 있는 값을 좌변에 있는 변수에 대입한다. <br>
변수에는 언제든 새로운 값을 대입할 수 있다. 이때 이전에 대입되어 있던 값은 사라진다.<br>
{% highlight python %}
value = 50
name = 'Hyeonjun Jin'

valie = 5
name = 'JIn Hyeonjun'
{% endhighlight %}
<hr>
## 다중 대입 구문
여러 변수 같은 값을 대입하거나 변수 여러 개에 값 여러 개를 동시 대입할 수 있다.
{% highlight python %}
value = result = param = 5
value1, value2, value3 = 5, 55, 555
{% endhighlight %}

## 복합 대입 구문
x = 5, y = 4 일 때<br> 
![]({{site.baseurl}}/images/python/20220305-2.png) <br>
왼쪽 x += y 로 작성한 결과와 x = x + y 로 작성한 결과는 같다. <br>
<strong>굳이 복합 대입 구문을 쓰는 이유?</strong> <br>
> cpu의 구조가 x = x + y 연산을 쓰는 것보다 x += y 와 같은 연산을 쓰는게 더 효율적이라고 한다. <br>복합 대입 구문을 사용하는 게 cpu 연산 속도가 빨라진다. 
<hr>
## 비교 연산자
값을 비교해서 참이면 True가 연산 결과가 되고 거짓이면 False가 연산 결과가 된다. (True와 False의 첫 글자는 대문자이다.) <br>
연산자는 ==, !=, >, <, >=, <= 로 구성된다. <br>

![]({{site.baseurl}}/images/python/20220305-3.png) <br>
<hr>

## 논리 연산자
논리 곱 연산자(and)<br>
논리 합 연산자(or)<br>
논리 부정 연산자(not) <br>
연산 결과는 참(True)과 거짓(False)가 된다.<br>
##### 논리 곱 연산(and)
True <strong>and</strong> True 일 경우 True<br>
True <strong>and</strong> False 일 경우 False<br>
##### 논리 합 연산자(or)
True <strong>or</strong> True 일 경우 True<br>
True <strong>or</strong> False 일 경우 True<br>
##### 논리 부정 연산자(not)
<strong>not</strong> True 일 경우 False <br>
<strong>not</strong> False 일 경우 True <br>
<hr>
###연산자 우선 순위
{% highlight python %}
a, b, c, d, e = 1, 2, 3, 4, 5
value = a * b % c - d / e
# 어떤 연산자를 먼저 연산해야 할까?
{% endhighlight %}
간단하게 외워야할 우선순위의 일반 규칙은 <strong>산술 연산자, 비교 연산자, 논리 연산자</strong> 순이다. <br>우선 순위가 같을 경우 왼쪽에서부터 순서대로 연산하며 곱셈과 나눗셈을 먼저 계산 후에 덧셈과 뺄셈을 계산한다. <br>
value 출력 시 1.2가 된다. 
<hr>
## 연습문제
> 밑변의 길이가 13이고 높이가 9인 삼각형의 넓이를 계산해서 출력한다. <br>프로그램을 작성하라.

{% highlight python %}
# 연습문제
# 밑변의 길이가 13이고 높이가 9인 삼각형의 넓이를 계산해서 출력한다.
width, height = 13, 9
area = 13 * 9 / 2
print('area =', area)
{% endhighlight %}
##### 출력
![]({{site.baseurl}}/images/python/20220305-4.png) <br>


