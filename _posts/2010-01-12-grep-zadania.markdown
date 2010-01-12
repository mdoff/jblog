---
layout: post
title: Grep zadania
---

# {{ page.title }}

<br />
##Zadanie 1
Znajdź wszystkie linie, które kończą się liczbami parzystymi:
{% highlight bash %}
egrep "[0-9]*[0,2,4,6,8]$" plik
{% endhighlight %}
