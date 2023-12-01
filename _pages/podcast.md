---
layout: page
title: export the sound
permalink: /podcast/
description: 'A podcast exploring how the industry moves music across borders, as told by the teams behind some of the most successful cross-cultural musicians.'
nav: true
nav_order: 2
horizontal: false
---

<!-- pages/podcast.md -->
<p>
 Follow on <a href="https://podcasters.spotify.com/pod/show/export-the-sound">Spotify</a> or <a href="https://podcasts.apple.com/us/podcast/export-the-sound/id1677755225">Apple Podcasts</a>.
</p>
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
