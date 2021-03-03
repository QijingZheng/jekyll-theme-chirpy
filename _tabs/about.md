---
title: About me
author: Qijing Zheng
icon: fas fa-info
years: [2010, 2014, 2016, 2017, 2018, 2019, 2020, 2021]
toc: true
order: 1
---

<table style="width:90%; margin: 0px 0px; padding:0px 6px; border: 0px solid #000000;">
    <tr>
        <td style="text-align:left">
            <span style="color: #008C93; font">
            <h3>
                Dr. Qijing Zheng （郑奇靖）
            </h3>
            </span>
			<br />
			Research Assistant Professor
			<br />
			Department of Physics
			<br />
			University of Science &amp; Technology of China
			<br />
			Hefei 230026, Anhui, China 
			<br />
			Email: <a href="mailto:zqj@ustc.edu.cn">zqj@ustc.edu.cn</a>
			<br />
        </td>
        <td style="text-align:right">
			<img style="border:2px solid #000000;" src="../assets/img/zqj.jpg" height="240px" />
		</td>
    </tr>
</table>
<br />

## Education

<table style="width:95%; margin: 20px 20px; padding:0px 6px; border: 0px solid #000000; height: 80px">
    <tr>
        <td>
            Sep. 2005 &mdash; Jul. 2009,
        </td>
        <td>BSc in Physics,</td>
        <td>University of Science &amp; Technology of China</td>
    </tr>
    <tr>
        <td>
            Sep. 2009 &mdash; Jun. 2016,
        </td>
        <td>PhD in Physics,</td>
        <td>University of Science &amp; Technology of China</td>
    </tr>
</table>

## Employment

<table style="width:95%; margin: 20px 20px; padding:0px 6px; border: 0px solid #000000; height: 80px">
    <tr>
        <td>
            Sep. 2016 &mdash; Sep. 2018,
        </td>
        <td>Postdoc</td>
        <td>University of Science &amp; Technology of China</td>
    </tr>
    <tr>
        <td>
            Sep. 2018 &mdash; now,
        </td>
        <td>Research Assistant Professor</td>
        <td>University of Science &amp; Technology of China</td>
    </tr>
</table>

## Publications

An up-to-date list is available on
<a href="https://scholar.google.com/citations?user=qeF95iQAAAAJ&hl=en" target="_blank">
Google Scholar.
</a>

<div>
    <sup>&#x23;</sup> for first/co-first author, * for corresponding/co-corresponding author.
</div>

{% for y in page.years reversed %}
  <h3  id="{{y}}" style="color: #008C93; border-bottom: 1px solid #f2f3f3;">{{y}}</h3>
  {% bibliography -f zqj_pub -q @*[year={{y}}]* %}
{% endfor %}
