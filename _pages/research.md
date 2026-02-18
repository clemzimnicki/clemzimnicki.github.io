---
layout: page
title: research
permalink: /research
nav: true
nav_order: 2

---
<p style="font-size:30px;"> how do we perceive and use colors in daily life? </p>

people differ in how they see color (and other visual features). these differences have been well documented. for my dissertation, I am studying these differences, and I aim to understand whether the differences are random, or whether there is some structure in how we differ (for example, if we fall into groups based on how we perceive color).


<p style="font-size:30px;"> how does visualization design affect interpretation? </p>

the visual features in a data visualization---such as colors, outlines, and symbols---can signficantly affect how people make sense of what they are seeing. in one of my lines of research, I have tried to understand how design can influence interpretation and decision-making. 

ultimately, this research can lead to a better understanding of how to make visualizations that are easy to interpret and use in real life. below are projects I've done on this topic!




<!-- pages/projects.md -->
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_projects = site.projects | where: "category", category -%}
  {%- assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
  {% endfor %}

{%- else -%}
<!-- Display projects without categories -->
  {%- assign sorted_projects = site.projects | sort: "importance" -%}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
{%- endif -%}
</div>

---