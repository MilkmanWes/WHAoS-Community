---
layout: default
title: Project List
permalink: /
---

<h1>All Currently Active Projects</h1>
<br>
{% for project  in site.projects %}
  <hr>
  {% if project.homepage %}
    <h2><a href="{{ project.homepage }}">{{ project.name }}</a></h2>
  {% elseif project.github %}
    <h2><a href="{{ project.github }}">{{ project.name }}</a></h2>
  {% else %}
    <h2>{{ project.name }}</h2>
  {% endif %}
  <h4>by: {{ project.author }}</h4>
  <p>{{ project.content | markdownify }}</p>
  <h6>{{ project.status }} | Release: {{ project.release }}
  {% elseif project.github %}
    <a href="{{ project.github }}">Github</a>
  {% endif %}
  </h6>

{% endfor %}

