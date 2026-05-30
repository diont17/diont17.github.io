---
layout: home
title: Home
---

## About

I am building this site as a home for notes, projects, and longer-form writing.

The shape is intentionally simple: a homepage, a few useful pages, and a blog that can grow over time.

## Featured

- [About]({{ "/about/" | relative_url }}) - a short introduction.
- [Now]({{ "/now/" | relative_url }}) - what I am focused on at the moment.
- [Blog]({{ "/blog/" | relative_url }}) - writing and notes.

## Recent Posts

{% if site.posts.size > 0 %}
  {% for post in site.posts limit: 3 %}
- [{{ post.title }}]({{ post.url | relative_url }}) <small>{{ post.date | date: "%-d %B %Y" }}</small>
  {% endfor %}
{% else %}
No posts yet.
{% endif %}
