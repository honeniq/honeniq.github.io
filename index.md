---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: post
title: トップページ
---

<h2>最近の記事</h2>
<ul>
  {% for post in site.posts limit:5 %}
    <li>
      <a href="{{ post.url }}">{{ post.date | date: '%Y-%m-%d' }} : {{ post.title }}</a>
    </li>
  {% endfor %}
</ul>

------

{% assign page = site.posts.first %}
{% assign content = page.content %}
<h2><a href="{{ page.url }}">{{ page.title }}</a></h2>
{{ content }}

