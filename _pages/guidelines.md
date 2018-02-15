---
layout: archive
title: Guidelines
permalink: /guidelines/
---
{% for guideline in site.guidelines %}
<div class="guideline">
<a href="{{guideline.url}}">{{guideline.title}} </a>
</div>
{% endfor %}

