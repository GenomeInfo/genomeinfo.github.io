---
title: Project index
---
# Projects

{% for repository in site.github.public_repositories %}
  {% comment %} omit the org site itself from the list {% endcomment %}
  {% if repository.name != "genomeinfo.github.io" %}
    {% comment %} if repo has a github pages site, link to it {% endcomment %}
    {% if repository.has_pages %}
 * [{{ repository.name }}]({{ repository.pages.html_url | append: "/" | append: repository.name}} )
    {% comment %} otherwise link to the github repo itself {% endcomment %}
    {% else %}
 * [{{ repository.name }}]({{ repository.html_url }})
    {% endif %}
  {% endif %}
{% endfor %}
