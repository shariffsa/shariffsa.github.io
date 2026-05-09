---
layout: page
title: Projects
subtitle: Selected work across supervisory analytics, ML, and data engineering.
permalink: /projects/
---

<p class="section-label">All Projects</p>

<div class="projects-grid">
{% for p in site.data.projects %}
  <div class="project-card">
    {% if p.status == 'soon' %}
      <span class="project-card__badge badge--soon">Coming Soon</span>
    {% elsif p.status == 'confidential' %}
      <span class="project-card__badge badge--conf">Confidential</span>
    {% elsif p.status == 'live' %}
      <span class="project-card__badge badge--live">Live</span>
    {% endif %}
    <p class="project-card__title">
      {% if p.demo %}<a href="{{ p.demo }}" target="_blank" rel="noopener">{{ p.name }}</a>
      {% elsif p.repo %}<a href="{{ p.repo }}" target="_blank" rel="noopener">{{ p.name }}</a>
      {% else %}{{ p.name }}{% endif %}
    </p>
    <p class="project-card__desc">{{ p.description }}</p>
    <p class="project-card__stack">{{ p.stack }}</p>
    {% if p.repo or p.demo %}
    <div class="project-card__links">
      {% if p.repo %}<a href="{{ p.repo }}" target="_blank" rel="noopener">GitHub →</a>{% endif %}
      {% if p.demo %}<a href="{{ p.demo }}" target="_blank" rel="noopener">Demo →</a>{% endif %}
    </div>
    {% endif %}
  </div>
{% endfor %}
</div>
