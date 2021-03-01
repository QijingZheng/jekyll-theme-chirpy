---
title: Publications
author: Qijing Zheng
icon: fas fa-newspaper
years: [2010, 2014, 2016, 2017, 2018, 2019, 2020, 2021]
toc: true
order: 2
---

An up-to-date list is available on
<a href="https://scholar.google.com/citations?user=qeF95iQAAAAJ&hl=en">
Google Scholar.
</a>

<div>
    <em>{% bibliography_count -f zqj_pub %}</em> papers in total.
    <br />
    <sup>&#x23;</sup> for first/co-first author, * for corresponding/co-corresponding author.
</div>


{% for y in page.years reversed %}
  <h3  id="{{y}}" style="color: #7a8288; border-bottom: 1px solid #f2f3f3;">{{y}}</h3>
  {% bibliography -f zqj_pub -q @*[year={{y}}]* %}
{% endfor %}
