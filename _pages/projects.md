---
layout: page
title: Projects
permalink: /projects/
description: Research and engineering projects.
nav: true
nav_order: 5
horizontal: false
---

<div class="projects">
  {%- assign sorted_projects = site.projects | sort: "importance" -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor -%}
  </div>
</div>
