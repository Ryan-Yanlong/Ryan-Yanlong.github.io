---
layout: page
title: Photography
permalink: /photography/
---

<div class="masonry">
{% for file in site.static_files %}
  {% if file.path contains "images/photography/" %}
    <a href="{{ site.baseurl }}{{ file.path }}" data-lightbox="gallery">
      <img src="{{ site.baseurl }}{{ file.path }}" loading="lazy">
    </a>
  {% endif %}
{% endfor %}
</div>


<style>
.masonry {
  column-count: 3;
  column-gap: 16px;
}

@media (max-width: 1000px) {
  .masonry {
    column-count: 2;
  }
}

@media (max-width: 600px) {
  .masonry {
    column-count: 1;
  }
}

.masonry a {
  display: block;
  margin-bottom: 16px;
  break-inside: avoid;
}

.masonry img {
  width: 100%;
  height: auto;
  border-radius: 4px;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.masonry img:hover {
  transform: scale(1.02);
  box-shadow: 0 6px 18px rgba(0,0,0,0.15);
}
</style>
