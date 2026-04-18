---
layout: page
title: Photography
permalink: /photography/
collection: pages
---

Here is my photo.

<div class="single-column">
{% for file in site.static_files %}
  {% if file.path contains "images/photography/" %}
    <a href="{{ site.baseurl }}{{ file.path }}" data-lightbox="gallery">
      <img src="{{ site.baseurl }}{{ file.path }}" loading="lazy" alt="">
    </a>
  {% endif %}
{% endfor %}
</div>

<style>
.single-column {
  max-width: 900px;  
  margin: 0 auto;
}

.single-column a {
  display: block;
  margin-bottom: 40px; 
}

.single-column img {
  width: 100%;
  height: auto;
  display: block;
  border-radius: 4px;
}
</style>
