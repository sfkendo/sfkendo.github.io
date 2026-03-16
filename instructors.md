---
layout: default
title: Instructors | SF Kendo
nav_current: instructors
banner_image: /assets/banners/shinai_1000_180.jpg
banner_alt: shinai_1000_180
---

<div class="entry-content">
  <style type="text/css">
    #gallery-1 { margin: auto; }
    #gallery-1 .gallery-item { float: left; margin-top: 10px; text-align: center; width: 25%; }
    #gallery-1 img { border: 2px solid #cfcfcf; }
    #gallery-1 .gallery-caption { margin-left: 0; }
  </style>

  <div id="gallery-1" class="gallery galleryid-12 gallery-columns-4 gallery-size-thumbnail">
    {% for instructor in site.data.instructors %}
    <dl class="gallery-item">
      <dt class="gallery-icon"><a title="{{ instructor.name }}"><img width="150" height="150" src="/assets/instructors/{{ instructor.image }}" class="attachment-thumbnail" alt="{{ instructor.name }}"></a></dt>
      <dd class="wp-caption-text gallery-caption">{{ instructor.name }}</dd>
    </dl>
    {% endfor %}
  </div>
</div>
