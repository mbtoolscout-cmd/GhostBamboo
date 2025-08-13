---
title: หน้าแรก
---

# รีวิว/เปรียบเทียบล่าสุด

<ul>
{% assign pages_list = site.pages | sort: 'date' | reverse %}
{% for p in pages_list %}
  {% if p.path contains 'posts/' %}
    <li>
      <a href="{{ p.url | relative_url }}">{{ p.title }}</a>
      <span class="muted"> — {{ p.date | date: '%Y-%m-%d' }}</span>
    </li>
  {% endif %}
{% endfor %}
</ul>