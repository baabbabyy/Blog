---
layout: page
title: "Picture"
description: "图片归档"
header-img: "img/orange.jpg"
---

![avatar](https://raw.githubusercontent.com/baabbabyy/baabbabyy.github.io/master/_pictures/2020_7_%E5%8A%B3%E5%8A%A8%E6%96%87%E5%8C%96%E9%A6%86%E8%8D%B7%E8%8A%B1.jpg)

目前还没想好具体放那些图片。恩 先看ins去吧

<ul class="listing">
{% for post in site.pictures %}
  {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
  {% if year != y %}
    {% assign year = y %}
    <li class="listing-seperator">{{ y }}</li>
  {% endif %}
  <li class="listing-item">
    <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
    <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>