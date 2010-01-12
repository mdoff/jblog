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
<br />
##Zadanie 2
Znajdź wszystkie linie zawierające adresy www z domenami .net lub .com lub .org
{% highlight bash %}
egrep "http://.*\.com *|http://.*\.org *|http://.*\.net *" plik
{% endhighlight %}

##Zadanie 3
{% highlight bash %}
egrep ".*@.*\." tekst  |grep -v com
{% endhighlight %}