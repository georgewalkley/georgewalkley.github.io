---
layout: page
title: Book Market Statistics
permalink: /bookmarketstatistics/
---

<a href="#gb">United Kingdom</a>
<a href="#eu">Europe</a>
<a href="#de">Germany</a>

<a name="gb"></a><h4>United Kingdom</a>

<table>
  {% for row in site.data.ukpa_annual %}
    {% if forloop.first %}
    <tr>
      {% for pair in row %}
        <th>{{ pair[0] }}</th>
      {% endfor %}
    </tr>
    {% endif %}

    {% tablerow pair in row %}
      {{ pair[1] }}
    {% endtablerow %}
  {% endfor %}
</table>

Data: <a href="https://www.publishers.org.uk/our-work/publications/">Publishers Association</a>, last updated 22 July 2020

<a name="eu"></a><h4>Europe</h4>

<table>
  {% for row in site.data.fep_estimates %}
    {% if forloop.first %}
    <tr>
      {% for pair in row %}
        <th>{{ pair[0] }}</th>
      {% endfor %}
    </tr>
    {% endif %}

    {% tablerow pair in row %}
      {{ pair[1] }}
    {% endtablerow %}
  {% endfor %}
</table>

Data: <a href="https://fep-fee.eu/European-Book-Publishing-1268">Federation of European Publishers</a>, last updated 18 January 2021

<a name="de"></a><h4>Germany</h4>

<table>
  {% for row in site.data.bdb_annual %}
    {% if forloop.first %}
    <tr>
      {% for pair in row %}
        <th>{{ pair[0] }}</th>
      {% endfor %}
    </tr>
    {% endif %}

    {% tablerow pair in row %}
      {{ pair[1] }}
    {% endtablerow %}
  {% endfor %}
</table>

Data: <a href="https://www.boersenverein.de/markt-daten/marktforschung/wirtschaftszahlen/">Börsenverein des Deutschen Buchhandels</a>, last updated 8 July 2020
