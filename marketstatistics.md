---
layout: page
title: Book Market Statistics
permalink: /bookmarketstatistics/
---

<table>
  {% for row in site.data.FEPEstimates %}
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
