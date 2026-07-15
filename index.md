---
layout: default
title: home
---

<div class="site-title">// TANGO_THREE_SIX</div>
<div class="site-subtitle">~ $ personal thoughts</div>

<div class="section-header">// recent posts</div>

{% if paginator.posts.size > 0 %}
<ul class="post-list">
  {% for post in paginator.posts %}
  <li>
    <div class="post-meta">{{ post.date | date: "%Y-%m-%d %H:%M" }}</div>
    <a href="{{ post.url }}">{{ post.title }}</a>
  </li>
  {% endfor %}
</ul>

<div class="pagination">
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path }}">&lt;&lt; newer</a>
  {% else %}
    <span></span>
  {% endif %}
  {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path }}">older &gt;&gt;</a>
  {% endif %}
</div>
{% else %}
<p>no posts yet. check back soon.</p>
{% endif %}