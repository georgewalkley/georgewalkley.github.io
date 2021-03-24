---
layout: page
title: Book Market Statistics
permalink: /bookmarketstatistics/
---

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
