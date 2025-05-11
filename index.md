---
layout: default
title: Home
---

## Latest Posts

<ul>
  {% for post in site.posts limit:10 %} {# Show latest 10 posts #}
    <li>
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p><small>{{ post.date | date: "%B %d, %Y" }}</small></p>
      {{ post.excerpt }} {# Or post.content for the full content #}
    </li>
  {% endfor %}
</ul>

<p><a href="{{ "/archive.html" | relative_url }}">All posts...</a></p>
