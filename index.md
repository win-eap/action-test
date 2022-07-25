---
---

Welcome to My Home Page

{% assign date = '2020-04-13T10:20:00Z' %}

- Original date - {{ date }}
- With timeago filter - {{ date | timeago }}

Some extra text to trigger a build.

List: 

<ul>
{% for member in site.data.list %}
<li>{{ member }}</li>
{% endfor %}
</ul>

Form Data: 

<table border=1>
  <tr>
    <th>Enter some words</th>
    <th>Choose an option</th>
  </tr>
{% for sheet in site.data.form_data.results %}
  {% for entry in sheet.result.rawData %}
    <tr>
      <td>{{ entry[1] }}</td>
      <td>{{ entry[2] }}</td>
    </tr>
  {% endfor %}
{% endfor %}
</table>

<a href="form_data.json">form data</a>
