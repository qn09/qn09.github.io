---
icon: fas fa-laptop-code
order: 6
title: Software
---

Chào mừng bạn đến với góc chia sẻ về Công nghệ & Lập trình phần mềm của tôi! Dưới đây là những câu chuyện và trải nghiệm thực tế trong hành trình phát triển nghề nghiệp của tôi.

---

{% assign software_posts = site.posts | where_exp: "item", "item.software == true" %}
{% for post in software_posts %}
<div class="software-card" onclick="window.location.href='{{ post.url | relative_url }}'">
  <h3 class="card-title">{{ post.title }}</h3>
  <div class="card-subtitle">{{ post.description }}</div>
  <div class="card-content">
    {{ post.content | strip_html | truncate: 200 }}
  </div>
</div>
{% endfor %}
