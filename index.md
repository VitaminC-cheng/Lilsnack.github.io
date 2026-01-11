---
layout: home
title: 首页
nav_order: 1
---

<style>
  .post-card {
    background-color: #f8f9fa;
    border: 1px solid #e9ecef;
    border-radius: 8px;
    padding: 20px;
    margin-bottom: 20px;
    box-shadow: 0 2px 4px rgba(0,0,0,0.05);
    transition: all 0.3s ease;
    display: block;
    color: inherit;
    text-decoration: none;
  }
  
  .post-card:hover {
    box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    transform: translateY(-2px);
  }
  
  .post-card h3 {
    margin-top: 0;
    margin-bottom: 10px;
  }
  
  .post-card .post-date {
    color: #6c757d;
    font-size: 0.9rem;
    margin-bottom: 15px;
  }
  
  .post-card .post-excerpt {
    color: #495057;
    line-height: 1.5;
  }
</style>

# 欢迎食用

This is my personal blog, created using just-the-docs theme.

## 最新文章

{% assign posts = site.posts | sort: 'date' | reverse %}
{% for post in posts %}
<a href="{{ post.url }}" class="post-card">
  <h3>{{ post.title }}</h3>
  <div class="post-date">{{ post.date | date: '%Y年%m月%d日' }}</div>
  <div class="post-excerpt">{{ post.content | strip_html | truncatewords: 30 }}</div>
</a>
{% endfor %}
