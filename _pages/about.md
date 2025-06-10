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

<style>
.author-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  gap: 2rem;
  margin-top: 2rem;
}
.author-box {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}
.author-avatar {
  width: 96px;
  height: 96px;
  border-radius: 50%;
  margin-bottom: 1rem;
}
.author-details h3 {
  margin: 0.2rem 0;
}
.author-links a {
  margin: 0 0.3rem;
  color: inherit;
}

.author-role-badge {
  display: inline-block;
  margin-left: 0.5em;
  padding: 0.15em 0.6em;
  border-radius: 1em;
  font-size: 0.5em;
  font-weight: 600;
  vertical-align: middle;
  text-transform: uppercase;
  letter-spacing: 0.05em;
}

.role-lead {
  background: #2e86de;
  color: #fff;
}
.role-core {
  background: #27ae60;
  color: #fff;
}
.role-member {
  background: #f1c40f;
  color: #222;
}
.role-alumni {
  background: #7f8c8d;
  color: #fff;
}
</style>

**Hi, we are Team LUIS! 👋**

We're an organized initiative from Luis Y. Ferrer Jr. Senior High School, dedicated to promoting 21st-century learning with technology. At our core, we believe that technology transcends mere devices; it's about expanding possibilities, chasing opportunities, and enriching knowledge.

Our club is a hub for anyone eager to leverage digital advancements to learn, build, and connect. Whether you're a beginner or looking to expand your horizons, we provide a vibrant space to explore new ideas, experiment with digital tools, and collaboratively discover how technology can enhance every aspect of our lives.

Let's prepare for a world constantly shaped by innovation. Join us to learn, grow, and shape our digital future.

## Meet our Team

<div class="author-grid">
  {% for entry in site.data.authors %}
    {% assign author = entry[1] %}
    {% include authorbox.html author=author %}
  {% endfor %}
</div>

