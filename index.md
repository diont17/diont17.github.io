---
layout: home
title: Home
---

## Hello 👋

I am an MRI physicist living in Wellington, New Zealand and working at Wellumio.

## Featured

- [About]({{ "/about/" | relative_url }}) - About me
- [Blog]({{ "/blog/" | relative_url }}) - I am collating my writing and publications here, please reach out if you have questions!

## Writings and academic publications

{% if site.posts.size > 0 %}
  {% for post in site.posts limit: 3 %}
- [{{ post.title }}]({{ post.url | relative_url }}) <small>{{ post.date | date: "%-d %B %Y" }}</small>
  {% endfor %}
{% else %}
No posts yet.
{% endif %}
