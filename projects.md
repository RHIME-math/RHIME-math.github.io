---
title: Projects
layout: projects
description: Projects
display_categories: [2023]
horizontal: false
---

# Projects

RHIME participants take on projects which apply statistical methods and technology to analyze socially relevant, accessible, and real-world problems.

<div class="projects">

  <!-- Display categorized projects -->
  {%- for category in page.display_categories %}
    <h2 class="category" >{{ category }}</h2>
    {%- assign categorized_projects = site.projects | where: "category", category -%}
    {%- assign sorted_projects = categorized_projects | sort: "weight" -%}

    <!-- Generate cards for each project -->
   <div class="row">
     {% for project in sorted_projects -%}
       {% include project.html -%}
     {% endfor %}
   </div>  

  {% endfor %}

</div>
