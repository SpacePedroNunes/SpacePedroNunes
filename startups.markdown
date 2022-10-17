---
title: Table new test
---

* site.data.datafile[0].description

{{ site.data.datafile[0].description }}

{{ site.data.datafile[1].description }}


* Table

<table>
  {% for row in site.data.datafile %}
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

*site.data.longstartups[0].description*

{{ site.data.longstartups[0]["Name"] }}
{{ site.data.longstartups[0]["BIC Status"] }}


