---
layout: default
title: Home
pageid: homepage
---

<div class="page-header">
<h1>{{ page.title }}</h1>
{% if page.tagline %}<p class="tagline">{{page.tagline}}</p>{% endif %}
</div>

<h2>Members</h2>
<ul>
{% for member in site.data.members %}
  <li>
    <a href="https://github.com/{{ member.github }}">
      {{ member.name }}
    </a>
  </li>
{% endfor %}
</ul>

