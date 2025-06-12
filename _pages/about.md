---
layout: splash
title: "About"
permalink: /about/
author_profile: false
classes: wide

header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/unsplash-image-1.webp
  actions:
    - label: "Join Us!"
      url: "https://www.facebook.com/lyfjshs.teamluis"
excerpt: "Let's explore how technology empowers you to grasp new concepts and bring your ideas to life, no matter your field."
---

<link rel="stylesheet" href="{{ '/assets/css/authorbox-styling.css' | relative_url }}">

**Hi, we are Team LUIS! 👋**

We're an organized initiative from [Luis Y. Ferrer Jr. Senior High School](https://www.facebook.com/DepedTayoLYFJSHS342285), dedicated to promoting 21st-century learning with technology. At our core, we believe that technology transcends mere devices; it's about expanding possibilities, chasing opportunities, and enriching knowledge.

Our club is a hub for anyone eager to leverage digital advancements to learn, build, and connect. Whether you're a beginner or looking to expand your horizons, we provide a vibrant space to explore new ideas, experiment with digital tools, and collaboratively discover how technology can enhance every aspect of our lives.

Let's prepare for a world constantly shaped by innovation. Join us to learn, grow, and shape our digital future.

## Meet our Team

<div id="batch-tabs" class="batch-tabs">
</div>

<div class="author-grid" id="author-grid">
  {% for entry in site.data.authors %}
    {% assign author = entry[1] %}
    <div class="author-box" data-batch="{{ author.batch | escape }}">
      {% include authorbox.html author=author %}
    </div>
  {% endfor %}
</div>

{% include batch-tabs.html %}