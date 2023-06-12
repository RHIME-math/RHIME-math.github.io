---
title: Projects
layout: projects
description: Projects
display_categories: [2023,2022]
horizontal: false
---

<!-- pages/projects.md -->
<div class="projects">
<!-- {%- if site.enable_project_categories and page.display_categories %} -->

  <!-- Display categorized projects -->
  {%- for category in page.display_categories %}
    <h2>{{ category }}</h2>
    {%- assign categorized_projects = site.projects | where: "category", category -%}
    {%- assign sorted_projects = categorized_projects | sort: "weight" -%}
  
    <!-- Generate cards for each project -->
    <div class="grid">
      {% for project in sorted_projects -%}
        {% include project.html -%}
      {% endfor %}
    </div>

  {% endfor %}

<!-- {%- else -%}
  
  <!-- Display projects without categories -->
  {%- assign sorted_projects = site.projects | sort: "weight" -%}
  
  <!-- Generate cards for each project -->
  <div class="grid">
    {% for project in sorted_projects -%}
      {% include project.html %}
    {%- endfor %}
  </div>

{%- endif -%}
-->
</div>
