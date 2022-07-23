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

Things: 

<ul>
{% for note in site.data.things.results[0].result.formatted %}
<li>{{ note.id }}: {{ note.note }}</li>
{% endfor %}
</ul>

[Things json](things.json)
