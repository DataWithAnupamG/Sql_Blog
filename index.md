---
layout: default
title: "SQL Blog"
---

<h1>SQL Blog</h1>

<div class="blog-container">
  {% for post in site.posts %}
    <a href="{{ site.baseurl }}{{ post.url }}" class="blog-card">
      <h2>{{ post.title }}</h2>
      <p>{{ post.excerpt | strip_html | truncatewords: 20 }}</p>
      <span class="date">{{ post.date | date: "%B %-d, %Y" }}</span>
    </a>
  {% endfor %}
</div>
