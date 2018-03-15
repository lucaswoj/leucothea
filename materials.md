---
title: Master Materials List
---

{% for project in site.projects %}

{% assign foo = project.content | split: "Materials</h3>" %}
{% assign bar = foo[1] | split: "<h3" | first | split: "<h2" | first %}

{% if bar %}

## [{{project.title}}]({{project.url}})

{{bar}}

{% endif %}

{% endfor %}
