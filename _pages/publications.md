---
layout: page
permalink: /publications/
title: publications
description: Publications in reversed chronological order. Generated by jekyll-scholar.
years: [2021, 2020, 2019, 2018, 2017, 2016, 2015, 2014, 2011]
years2: [2019,2017,2015, 2014, 2013, 2012]
years3: [2021]
nav: true
---

<div class="publications">


 <h2>Accepted papers</h2> 

{% for y in page.years %}
  <h3 class="year">{{y}}</h3>
  {% bibliography -f papers.bib -q @*[year={{y}}]* %}
{% endfor %}

<h2> Submitted and in preparation </h2>

{% for y in page.years3 %}
  <h3 class="year">{{y}}</h3>
  {% bibliography -f Ongoing.bib -q @*[year={{y}}]* %}
{% endfor %}

<h2> Demo abstracts, Workshop papers and Works-in-Progress </h2>

{% for y in page.years2 %}
  <h3 class="year">{{y}}</h3>
  {% bibliography -f wips.bib -q @*[year={{y}}]* %}
{% endfor %}

</div>
