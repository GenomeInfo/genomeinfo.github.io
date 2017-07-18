---
title: Project index
---
# Projects

{% for repository in site.github.public_repositories %}
  {% if repository.name != "genomeinfo.github.io" %}
  {% if repository.has_pages %}
  * [{{ repository.name }}]({{ repository.pages.html_url }})
{% comment %}  * [{{ repository.name }}](https://{{ site.github.owner_name }}.{{ site.github.pages_hostname }}/{{ repository.name }}) {% endcomment %}
  {% endif %}
  {% endif %}
{% endfor %}
