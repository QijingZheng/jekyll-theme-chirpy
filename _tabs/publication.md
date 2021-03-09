---
title: Publications
author: Qijing Zheng
icon: fas fa-newspaper
years: [2010, 2014, 2016, 2017, 2018, 2019, 2020, 2021]
journals: "Journal of Physical Chemistry Letters, Physical Review B, Journal of the American Chemical Society, Journal of Physical Chemistry C, Science Advances, Nano Letters, Journal of Physics Condensed Matter, Wiley Interdisciplinary Reviews: Computational Molecular Science, Science China Chemistry, Physical Review Letters, Journal of Physical Chemistry A, Journal of Materials Chemistry C, Journal of Materials Chemistry A, Electronic Structure, Communications Physics" 
toc: true
order: 2
---

An up-to-date list is available on
<a href="https://scholar.google.com/citations?user=qeF95iQAAAAJ&hl=en" target="_blank">
Google Scholar.
</a>

<!---
<div>
    <h3>Publication Summary</h3>
    <em>{% bibliography_count -f zqj_pub %}</em> papers in total, including
    <br/>
    <div class="container">
        {% assign journals = page.journals | split: ", " %}
        {% for j in journals %}
            <span class='btn btn-outline-default btn-sm'>
                <span style="color: #048D67"> <i>{{ j }}</i> </span>:
                {% bibliography_count -f zqj_pub -q @*[journal={{j}}] %}
            </span>
        {% endfor %}
    </div>
</div>

<br />
--->

<div>
    <h3>Publication Summary</h3>
    <em>{% bibliography_count -f zqj_pub %}</em> papers in total, including
    <br/>
    <div class="container">
        {% assign journals = page.journals | split: ", " %}
        {% for j in journals %}
            {% assign jid =  j | replace: " ", "_"  | replace: ":", "-" %}
            <button type="button" class="btn btn-sm mr-1 mt-2" data-toggle="modal" data-target="{{ jid | prepend: '#my_' }}">
                <span style="color: #048D67"> <i>{{ j }}</i> </span>:
                {% bibliography_count -f zqj_pub -q @*[journal={{j}}] %}
            </button>
            <div class="modal fade" id="{{ jid | prepend: 'my_' }}">
              <div class="modal-dialog modal-dialog-centered" style="max-width: 45%!important;" role="document">
                <div class="modal-content">
                  <div class="modal-header">
                    <button type="button" class="close" data-dismiss="modal">&times;</button>
                  </div>
                  <div class="modal-body">
                    <div>
                        {% bibliography -f zqj_pub -q @*[journal={{j}}] -T bib_2 %}
                    </div>
                  </div>
                  <div class="modal-footer">
                    <button type="button" class="btn btn-default" data-dismiss="modal">Close</button>
                  </div>
                </div>
              </div>
            </div>
        {% endfor %}
    </div>
</div>

<br />
<div>
    A full publication list sorted by year can be found below, where
    <sup>&#x23;</sup> is used to indicate first/co-first author and * for
    corresponding/co-corresponding author.
</div>

{% for y in page.years reversed %}

  <h3  id="{{y}}" style="color: #7a8288; border-bottom: 1px solid #f2f3f3;">{{y}}</h3>
  {% bibliography -f zqj_pub -q @*[year={{y}}]* %}
{% endfor %}
