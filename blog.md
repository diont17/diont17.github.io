---
title: Blog
permalink: /blog/
---

# Blog

{% if site.posts.size > 0 %}
  <ol class="post-list">
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%-d %B %Y" }}</time>
      {% if post.excerpt %}
        <p>{{ post.excerpt | strip_html | truncate: 150 }}</p>
      {% endif %}
    </li>
  {% endfor %}
  </ol>
{% else %}
No posts yet.
{% endif %}
