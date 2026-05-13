---
layout: page
title: Complex Biology
---

*Everything where understanding requires data analysis — high-dimensional data that needs breaking down, and where the descriptors of what's moving or changing aren't easy to name.*

{% assign posts = site.posts | where_exp: "post", "post.categories contains 'bioml'" %}
{% if posts.size > 0 %}
{% for post in posts %}
<h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
<p>{{ post.date | date: "%B %-d, %Y" }}</p>
{% endfor %}
{% else %}
<p><em>Posts coming soon.</em></p>
{% endif %}
