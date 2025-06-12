---
layout: splash
title: "About"
permalink: /about/
author_profile: false
classes: wide

header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/unsplash-image-1.jpg
  actions:
    - label: "Join Us!"
      url: "https://github.com/mmistakes/minimal-mistakes/"
excerpt: "Let's explore how technology empowers you to grasp new concepts and bring your ideas to life, no matter your field."
---

<link rel="stylesheet" href="{{ '/assets/css/authorbox-styling.css' | relative_url }}">

**Hi, we are Team LUIS! 👋**

We're an organized initiative from Luis Y. Ferrer Jr. Senior High School, dedicated to promoting 21st-century learning with technology. At our core, we believe that technology transcends mere devices; it's about expanding possibilities, chasing opportunities, and enriching knowledge.

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

<script>
document.addEventListener("DOMContentLoaded", function() {
  // 1. Gather unique batches from author boxes' data-batch attributes
  const authorBoxes = document.querySelectorAll('.author-box[data-batch]');
  const batches = Array.from(authorBoxes)
    .map(box => box.getAttribute('data-batch'))
    .filter(Boolean)
    .filter((v, i, a) => a.indexOf(v) === i); // unique

  // 2. Render tab buttons
  const tabContainer = document.getElementById('batch-tabs');
  if (!tabContainer) return;
  tabContainer.innerHTML = batches.map((batch, idx) => `
    <button
      class="batch-tab${idx===0 ? ' active' : ''}"
      data-batch="${batch}"
      type="button"
      tabindex="0"
      aria-selected="${idx===0 ? 'true' : 'false'}"
    >${batch}</button>
  `).join('');

  // 3. Filtering logic
  function showBatch(batch) {
    authorBoxes.forEach(box => {
      if (box.getAttribute('data-batch') === batch) {
        box.style.display = '';
      } else {
        box.style.display = 'none';
      }
    });
  }
  // Show first batch on load
  showBatch(batches[0]);

  // 4. Tab switching event
  tabContainer.addEventListener('click', e => {
    const btn = e.target.closest('.batch-tab');
    if (!btn) return;
    // Update active state
    tabContainer.querySelectorAll('.batch-tab').forEach(tab => {
      tab.classList.toggle('active', tab === btn);
      tab.setAttribute('aria-selected', tab === btn ? 'true' : 'false');
    });
    showBatch(btn.getAttribute('data-batch'));
  });
});
</script>