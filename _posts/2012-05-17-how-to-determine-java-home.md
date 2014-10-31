---
layout: post
category : linux
tagline: ""
tags : [debian, how-to, java]
---
{% include JB/setup %}

Simple run the following command

{% highlight bash %}
export -p JAVA_HOME=$(readlink -f /usr/bin/java | sed "s:bin/java::")
{% endhighlight %}

{% gist 5814513 %}
