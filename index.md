---
layout: default
title: Project List
permalink: /
---

<h1>All Currently Active Projects</h1>
<br>
{% for project  in site.projects %}
  <hr>
  <h2>
  {% if project.homepage %}
    <a href="{{ project.homepage }}">{{ project.name }}</a>
  {% else %}
    {{ project.name }}
  {% endif %}
  </h2>
  <h4>by: {{ project.author }}</h4>
  <p>{{ project.content | markdownify }}</p>
  <h6>{{ project.status }} | Release: {{ project.release }}
  {% if project.github %}
    <a href="{{ project.github }}">Github</a>
  {% endif %}
  </h6>

{% endfor %}

