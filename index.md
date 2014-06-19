---
layout: default
title: Home
pageid: homepage
---
{% include JB/setup %}

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


## Docs

<ul class="post">
{% for pg in site.pages %}
  {% if pg.index contains page.pageid %}
    <li><a href="{{ BASE_PATH }}{{ pg.url }}">{{ pg.title }}</a></li>
  {% endif %}
{% endfor %}
</ul>

## Recent 20 Posts

<ul class="posts">
{% for post in site.posts | limit: 20 %}
<li><span class="date"><time>{{ post.date | date: "%Y-%m-%d" }}</time></span><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a>{% if post.author %}<span class="author"> by {{ post.author }}{% endif %}</span></li>
{% endfor %}
</ul>

