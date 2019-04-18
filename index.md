---
layout: home
id: home
title: Homepage
---

{% assign pages = site.projects | sort:"year" %}
<ul class="projects">
  {% for p in pages reversed %}<li>
      <a href="{{ p.url }}">
        <img src="{{ p.image }}" alt="{{ p.title }} screenshot" />
        {{ p.title }}
      </a>
  </li>{% endfor %}
</ul>
