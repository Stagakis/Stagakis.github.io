---
layout: page
title: Projects
permalink: /projects/
---

<ul class="post-list">
<!-- Render Projects. -->  
  {%- if site.projects.size > 0 -%}
  <div>
    <ul class="post-list myDiv">
      {%- for post in site.projects -%}
      <li>
        {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
        <figure class="figure">
          <a href="{{ post.url | relative_url }}">
            <img class="thumbnail" border="2" alt="" src="{{ post.image_file }}"></a>      
          <figcaption class="figcaption">
            {{ post.title | escape }}
            <p class="post-meta">{{ post.date | date: date_format }}</p>
          </figcaption>
        </figure>

      </li>
      {%- endfor -%}
    </ul>
  </div>
  {%- endif -%}
</ul>