---
layout: archive
title: Articles
permalink: /articles/
---
{% for article in site.articles %}
<div class="article">
<a href="{{article.url}}">{{article.title}} </a>
<p> {{article.excerpt}} </p>
</div>
{% endfor %}

