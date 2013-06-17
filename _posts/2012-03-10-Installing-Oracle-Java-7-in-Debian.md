---
layout: post
category : linux
tagline: "via Repository"
tags : [debian, how-to, java, jdk, jre]
---
{% include JB/setup %}

To add the WebUpd8 Oracle Java PPA repository to the Software Sources in Debian (tested on Debian Squeeze, but it should work with any Debian version), use the following commands

{% highlight bash %}
su -
echo "deb http://ppa.launchpad.net/webupd8team/java/ubuntu precise main" | tee -a /etc/apt/sources.list
echo "deb-src http://ppa.launchpad.net/webupd8team/java/ubuntu precise main" | tee -a /etc/apt/sources.list
apt-key adv --keyserver keyserver.ubuntu.com --recv-keys EEA14886
apt-get update
apt-get install oracle-java7-installer
exit
{% endhighlight %}

To automatically set up the Java 7 environment variables, install the following package:

{% highlight bash %}
sudo apt-get install oracle-java7-set-default
{% endhighlight %}
