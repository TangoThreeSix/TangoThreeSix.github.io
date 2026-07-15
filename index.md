---
layout: default
title: home
---

<div class="site-title">// TANGO_THREE_SIX</div>
<div class="site-subtitle">~ $ personal thoughts</div>

<div class="section-header">// recent posts</div>

{% if site.posts.size > 0 %}
<ul class="post-list">
  {% for post in site.posts %}
  <li>
    <div class="post-meta">{{ post.date | date: "%Y-%m-%d %H:%M" }}</div>
    <a href="{{ post.url }}">{{ post.title }}</a>
  </li>
  {% endfor %}
</ul>
{% else %}
<p>no posts yet. check back soon.</p>
{% endif %}