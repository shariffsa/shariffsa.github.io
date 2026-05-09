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
    {% if p.status == 'soon' %}<span class="card-badge badge--soon">Coming Soon</span>
    {% elsif p.status == 'confidential' %}<span class="card-badge badge--conf">Confidential</span>
    {% elsif p.status == 'live' %}<span class="card-badge badge--live">Live</span>{% endif %}
    <p class="card-title">
      {% if p.demo %}<a href="{{ p.demo }}" target="_blank" rel="noopener">{{ p.name }}</a>
      {% elsif p.repo %}<a href="{{ p.repo }}" target="_blank" rel="noopener">{{ p.name }}</a>
      {% else %}{{ p.name }}{% endif %}
    </p>
    <p class="card-desc">{{ p.description }}</p>
    <p class="card-stack">{{ p.stack }}</p>
    {% if p.repo or p.demo %}
    <div class="card-links">
      {% if p.repo %}<a href="{{ p.repo }}" target="_blank" rel="noopener">GitHub →</a>{% endif %}
      {% if p.demo %}<a href="{{ p.demo }}" target="_blank" rel="noopener">Demo →</a>{% endif %}
    </div>
    {% endif %}
  </div>
{% endfor %}
</div>
