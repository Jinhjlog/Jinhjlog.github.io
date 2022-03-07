---
layout: post
title: 2일차. Python 자료형과 입출력
image: python.png
date: 2022-03-06 13:20:20 +0200
tags: [python]
categories: python
---
## 자료형
값(data)의 종류, 자료형에 따라 프로그램에서 값을 다루는 방법이 달라진다.
<br>
## 파이썬에서 다루는 자료형
파이썬에서 다루는 자료형은 integer(정수), Boolean(참 또는 거짓), floating point(소수점), complex(복소수 표현), String(문자열), List, Tuple, set(집합 개념), Dictionary(값과 값들을 서로 연결해 놓은 것)

## 문자열
문자들의 집합인 문자열을 다루는 자료형
{% highlight python %}
# 제어 문자 출력
print('\n, \t, \', \", \\')
# 문자열들을 덧셈 연산자로 연결 할 수 있다. (문자열은 문자열과만 연결 가능)
print('Fire + Bird : '+'Fire' + 'Bird')
# 곱셈 연산자를 이용하여 반복
print('Hi!*2 : '+'Hi!'*2)
{% endhighlight %}
![]({{site.baseurl}}/images/python/20220306/20220306-3.png)
<hr>
## 함수와 메써드
* function : 함수, 특정한 동작을 수행하는 기능 // 예시 : len(), print() <br>
* method : 메써드, 함수와 비슷하다 // 예시 : message.upper() <br>
메써드는 함수와 다르게 이름만으로 호출 될 수 없다. (예시 참고) <br>

> 문자열 메써드
{% highlight python %}
mail = 'Wellcome!!'
# 문자열을 대문자로 변환
print('mail.upper() ->', mail.upper())
# 문자열을 소문자로 변환
print('mail.lower() ->', mail.lower())
# 문자열에 포함된 특정 문자의 개수 계산
print('mail.count(l) ->', mail.count('l'))
{% endhighlight %}
![]({{site.baseurl}}/images/python/20220306/20220306-4.png)
<hr>
# 자료형 변환 함수
자료형 다음에 괄호를 사용하면 된다.
자료형(값)
예시 : int(x), complex(x, y), float(x), str(x) 등등 
<hr>
## 표준 출력
컴퓨터 시스템에서 가장 기본이 되는 출력 장치

<strong>print 함수 : 표준 출력에 지정한 값을 출력하고 개행</strong>
{% highlight python %}
print('Hello World!!')
{% endhighlight %}
![]({{site.baseurl}}/images/python/20220306/20220306-1.png)
<hr>
## 변수 정의와 출력
{% highlight python %}
value = 10
# print 함수를 이용해 변수 value를 출력한다.
print(value)

# value = 10
# 위와 같이 출력하기 위해서는 문자열을 만들어야 한다.
print('value = ' + str(value))
# or
print('value =', value)
# print 함수에서 여러 값을 출력할 수 있으며 쉼표(,)로 구분한다. 각 값들은 빈칸으로 구분되어 출력
{% endhighlight %}
![]({{site.baseurl}}/images/python/20220306/20220306-2.png) <br>
<hr>
## sep인자
빈칸이 아닌 다른 값으로 각각의 값들을 구분하고자 할 때 사용한다
{% highlight python %}
print(1, 2, 3)          #1 2 3
print(1, 2, 3, sep=", ")  #1, 2, 3
print(1, 2, 3, sep=",")  #1,2,3
print(2580, 1080, sep='x')  # 2580x1080
{% endhighlight %}
![]({{site.baseurl}}/images/python/20220306/20220306-5.png) <br>

## end 인자
print 함수는 마지막에 개행문자를 출력하게 되는데 만약 이를 다른 값으로 바꾸고 싶다면 end인자를 사용하면 된다.
{% highlight python %}
value = 30
print('value = ', end='')   # 'value = '
print(value)                # 30\
# end 인자를 설정해서 마지막에 출력되는 개행 문자를 제거 한다.
{% endhighlight %}
![]({{site.baseurl}}/images/python/20220306/20220306-6.png) <br>
<hr>
## 형식화된 문자열(formatted string)
{% highlight python %}
value = 30
result = value / 3  # result = 10
print('value =', value, 'value / 3 =', result)
# 첫 번째 값은 위치가 0, 두 번째 값은 위치가 1 이 된다.
print('value = {0} value / 3 = {1}'.format(value, result))
# 값들이 순서대로 들어간다면 0과 1을 생략할 수 있다.
print('value = {} value / 3 = {}'.format(value, result))
{% endhighlight %}
![]({{site.baseurl}}/images/python/20220306/20220306-7.png) <br>




