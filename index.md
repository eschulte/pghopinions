---
layout: default
title: PGH Opinions
---

Opinions
========

{% assign row = 0 %}
{% assign sorted = collections.opinion | reverse %}
{% for opinion in sorted %}

{% if row == 0 %}
<div class="w3-row-padding">
{% endif %}

<div class="w3-half w3-margin-bottom">
<div class="w3-container w3-card">

## [{{ opinion.data.title }}]({{ opinion.url | url }})

{{ opinion.templateContent }}

</div>
</div>

{% if row == 1 %}
</div>
{% assign row = 0 %}
{% endif %}

{% assign row = row | plus: 1 %}
{% endfor %}
