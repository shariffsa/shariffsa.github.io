---
title: Projects
layout: page
permalink: /projects/
---

Below are selected projects. This page is generated from `_data/projects.yml` to keep things tidy.

{% assign items = site.data.projects %}
<div class="projects">
  {% for p in items %}
  <div class="project">
    <h3><a href="{{ p.url | default: '#' }}" target="_blank" rel="noopener">{{ p.name }}</a></h3>
    <p>{{ p.description }}</p>
    <ul>
      <li><strong>Stack:</strong> {{ p.stack }}</li>
      {% if p.repo %}<li><a href="{{ p.repo }}" target="_blank" rel="noopener">GitHub repo</a></li>{% endif %}
      {% if p.demo %}<li><a href="{{ p.demo }}" target="_blank" rel="noopener">Live demo</a></li>{% endif %}
    </ul>
  </div>
  <hr/>
  {% endfor %}
</div>
