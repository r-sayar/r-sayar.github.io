---
layout: page
title: Drafts
---

Published but unfinished. These are posts I've put out but am still working on — v1s meant to be improved.

{% assign posts = site.posts | where_exp: "post", "post.categories contains 'drafts'" %}
{% if posts.size > 0 %}
{% for post in posts %}
<h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
<p>{{ post.date | date: "%B %-d, %Y" }}</p>
{% endfor %}
{% else %}
<p><em>Nothing here yet.</em></p>
{% endif %}
