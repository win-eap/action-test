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

<table>
  <tr>
    <th>Enter some words</th>
    <th>Choose an option</th>
  <tr>
{% for sheet in site.data.form_data %}
  {% for entry in sheet.result.formatted %}
  <tr>
    <td>{{ entry['Enter some words'] }}</td>
    <td>{{ entry['Choose an option'] }}</td>
  </tr>
  {% endfor %}
{% endfor %}
</taable>

[Things json](things.json)
