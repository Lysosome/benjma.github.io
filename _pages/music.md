---
layout: page
title: music
permalink: /music/
description: 
nav: true
nav_order: 5
horizontal: false
---
for more, visit dj lysosome on <b><a href="https://www.youtube.com/channel/UCSlC9SxzWz8qP99eWa2Chrw">youtube</a></b> or <b><a href="https://open.spotify.com/artist/22AirBWaCuTbdCtSCMbWdP">spotify</a></b>.

<!-- pages/music.md -->
<div class="projects">
  {%- assign sorted_projects = site.music_projects | sort: "importance" -%}
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
