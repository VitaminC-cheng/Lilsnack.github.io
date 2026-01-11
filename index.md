---
layout: home
title: 首页
nav_order: 1
---

# 欢迎食用

This is my personal blog, created using just-the-docs theme.

## 最新文章

{% assign posts = site.posts | sort: 'date', 'desc' %}
{% for post in posts %}
### [{{ post.title }}]({{ post.url }})
{{ post.date | date: '%Y年%m月%d日' }}
{{ post.content | strip_html | truncatewords: 30 }}
{% endfor %}
