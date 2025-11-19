---
layout: default
title: Home
---

## Latest Posts

<ul>
  {% for post in site.posts limit:10 %}
    <li>
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p><small>{{ post.date | date: "%Y-%m-%d" }}</small></p>
      {{ post.excerpt }}
    </li>
  {% endfor %}
</ul>

<p><a href="{{ "/archive.html" | relative_url }}">All posts...</a></p>
