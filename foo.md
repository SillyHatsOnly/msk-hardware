---
layout: default
title: foo это тест
---

{% for article in site.articles %}
 <p><a href="{{ article.url }}">{{ article.title }}</a><br/>
   {{ article.foo }}</p>
{% endfor %}
