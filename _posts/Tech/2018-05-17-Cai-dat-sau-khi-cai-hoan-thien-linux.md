---
layout: post
title: Cài đặt sau khi cài hoàn thiện Linux
subtitle: Những tùy chỉnh, ứng dụng hay sử dụng
category: [Tech]
comments: false
---

**Chỉnh thời gian Windows và Linux cùng chạy một lúc**

{% highlight javascript linenos %}
timedatectl set-local-rtc 1 --adjust-system-clock
{% endhighlight %}


**Cài Google Chrome**

{% highlight javascript linenos %}
wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add -
sudo sh -c 'echo "deb http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google.list'
sudo apt-get update
sudo apt-get install google-chrome-stable
{% endhighlight %}


**Sử dụng packages:**

{% highlight javascript linenos %}
sudo apt-get install <package>
{% endhighlight %}

| ttf-mscorefonts-installer (Font)	 | build-essential | 
| default-jre (Java)	 | default-jdk (Java) | 
| vlc | gnuplot |
| inkscape | gimp | 
| qbittorrent | ubuntu-restricted-extras (Media)|
| curl | git (Github) |
| unity-tweak-tool	|

**Cài packages môi trường làm website:**

{% highlight javascript linenos %}
sudo apt-get install npm 
sudo apt-get install nodejs 
sudo npm install -g browser-sync 
{% endhighlight %}

{% highlight javascript linenos %}
browser-sync start --server --directory --files "*"   //Mở trang xem đường dẫn 
{% endhighlight %}

**Cài skype:**

{% highlight javascript linenos %}
dpkg -s apt-transport-https > /dev/null || bash -c "sudo apt-get update; sudo apt-get install apt-transport-https -y"
curl https://repo.skype.com/data/SKYPE-GPG-KEY | sudo apt-key add -
echo "deb [arch=amd64] https://repo.skype.com/deb stable main" | sudo tee /etc/apt/sources.list.d/skype-stable.list
sudo apt-get update
sudo apt-get install skypeforlinux
{% endhighlight %}

**Cài ibus:**

{% highlight javascript linenos %}
sudo apt-get install ibus-unikey    //Vietnamese
sudo apt-get install mozc           //Japanese
ibus restart
{% endhighlight %}
