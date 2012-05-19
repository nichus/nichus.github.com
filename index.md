---
layout: default
title: Icebergh - Just a waste of bits
---
{% include JB/setup %}

<div id="content" class="">
{% for post in site.posts offset: 0 limit: 10 %}
  <div class="post">
    <div class="date-box">
      <span class="date">{{ post.date | date: "%d" }}</span>
      <span class="month">{{ post.date | date: "%b" | upcase }}</span>
      <span class="year">{{ post.date | date: "%Y" }}</span>
    </div>
    <h2><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h2>
    <div class="meta">
      <div class="">Tagged as: {{ post.tags }}</div>
    </div>
    <div class="entrybody">
      {{ post.content | strip_html | truncatewords: 100 }}
    </div>
  </div>
  <br />
{% endfor %}
</div>
