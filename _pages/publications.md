---
layout: page
permalink: /publications/
title: publications
description: 
years: [2024, 2023, 2022, 2021]
nav: true
order: 2
navigation_weight: 20
---

<div class="publications">

<h2 class="year">preprints</h2>
{% bibliography -f papers -q @*[preprint=true]* %}

{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}} && preprint!=true]* %}
{% endfor %}

</div>