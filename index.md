---
layout: page
title: Icebergh - Just a waste of bits
---
{% include JB/setup %}

<div id="content" class="">
{% for post in site.posts offset: 0 limit: 10 %}
  <div class="post">
    <h2><a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></h2>
    <div class="entrybody">
      {{ post.content | strip_html | truncatewords: 100 }}
    </div>
    <div class="meta">
      <ul>
        <li class="date">Posted on: {{ post.date | date_to_string }}</li>
        <li class="tags">Tagged: {{ post.tags }}</li>
      </ul>
    </div>
  </div>
{% endfor %}
</div>
