---
layout: page
title: Corperial
---

Technologies of the body — tissue engineering, ex vivo systems, keeping biology alive outside its native context, and closing the gap between in vitro and in vivo.

{% assign posts = site.posts | where_exp: "post", "post.categories contains 'corporeal-technologies'" %}
{% if posts.size > 0 %}
{% for post in posts %}
<h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
<p>{{ post.date | date: "%B %-d, %Y" }}</p>
{% endfor %}
{% else %}
<p><em>Posts coming soon.</em></p>
{% endif %}
