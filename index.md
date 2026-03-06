---
layout: home
title: 
---

<div class="project-grid">
{% assign sorted_projects = site.projects | sort: 'title' %}
{% for project in sorted_projects %}
  <article class="project-card">
    <a href="{{ project.url | relative_url }}">
      {% if project.image %}
        <img src="{{ project.image | relative_url }}" alt="Screenshot of {{ project.title }}" loading="lazy">
      {% endif %}
      <h2>{{ project.title }}</h2>
      {% if project.summary %}<p>{{ project.summary }}</p>{% endif %}
    </a>
  </article>
{% endfor %}
</div>
