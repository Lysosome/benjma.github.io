---
layout: page
title: podcast
permalink: /podcast/
description: '<b>export the sound</b>: how the industry moves music across borders, as told by the teams behind some of the most successful cross-cultural musicians. episodes coming soon.'
nav: true
nav_order: 2
horizontal: false
---

<!-- pages/podcast.md -->
<div class="projects">

{%- assign sorted_projects = site.podcast_episodes | sort: "importance" -%}
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
</div>
