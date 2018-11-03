---
layout: default
title: Project List
permalink: /
---

<h1>All Currently Active Projects</h1>
<br>
{% for project  in site.projects %}
  <hr>
  <h2><a href="{{ project.homepage }}">{{ project.name }}</a></h2>
  <h4>by: {{ project.author }}</h4>
  <p>{{ project.content | markdownify }}</p>
  <h6>{{ project.status }} | Release: {{ project.release }} | <a href="{{ project.github }}">Git Repo</a></h6>

{% endfor %}

