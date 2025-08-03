---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Home
permalink: /
images:
  - /static/figs/ma/general_1.png
  - /static/figs/ma/general_2_2.png
  - /static/figs/ma/medical_2.png
  - /static/figs/ma/input_mask_full_example.png
#   - /static/figs/ma/ModelEval.drawio.png
  - /static/figs/ds/dl_style_transfer.png
  - /static/figs/ds/world_migration_map.png
  - /static/figs/ds/vs_nutrition_wide.png
#  - /static/figs/ds/vs_kibana.png
  - /static/figs/ds/tweetskb_available_vs_unavailable_bigger.png

---

# Hello!

<div style="display: flex; align-items: center; justify-content: space-between;">
  <div style="flex: 1; padding-right: 20px;">
    <p>
        Hi my name is Oliver Stritzel and I am a Data Engineer and Data Scientist based in Nuremberg, Germany. I try to teach machines to do useful stuff to make your life easier.
    </p>
    <p>
        I have worked as a data scientist for over 5 years and as a big data engineer for 3 years previously. 
    </p>
  </div>
  <div>
    <img src="static/foto_oval.png" alt="me.png" style="width: 150px;">
  </div>
</div>


Feel free to check out my <a href="/static/cv_en.pdf" download>cv</a>, my [projects]({{ site.baseurl }}/projects/) and <a href="mailto:{{ site.email }}">reach out</a>!


### Exposé

<div class="swiper">
  <div class="swiper-wrapper">
    <!-- Slides -->
    {% for image in page.images %}
      <div class="swiper-slide">
        <img src="{{ image }}" alt="Slide {{ forloop.index }}">
      </div>
    {% endfor %}  </div>

  <!-- Pagination and Navigation -->
  <div class="swiper-pagination"></div>
  <div class="swiper-button-prev"></div>
  <div class="swiper-button-next"></div>
</div>