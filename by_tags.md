---
layout: page
title: By Tags
---

{% for tag in site.tags %}
  <h3>{{ tag[0] }}</h3>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a>, {{ post.date | date: "%B %Y" }}</li>
    {% endfor %}
  </ul>
{% endfor %}
