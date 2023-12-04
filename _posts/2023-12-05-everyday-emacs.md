---
layout: post
title:  "Everyday Emacs"
date:   2023-12-05 01:54:46 +0900
categories: emacs
---

{% highlight bash %}
cd $(ghq list -p | grep emacs) \
&& git checkout emacs-29 \
&& git pull \
&& make clean  \
&& ./autogen.sh \
&& ./configure --with-native-compilation --with-ns --without-x \
&& make -j10 \
&& make install \
&& open nextstep
{% endhighlight %}

Emacs.app の移動は Finder でやる

{% highlight bash %}
ln -sf /Applications/Emacs.app/Contents/MacOS/bin/* ~/bin
{% endhighlight %}


----


- [macOSにネイティブコンパイル対応のEmacs29を導入する（Orgファイル/Makefileで管理）](https://zenn.dev/xbonewalker/articles/35c4fb424bbfa7)
