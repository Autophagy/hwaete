---
layout: page
---
{% include JB/setup %}

Hwæt! This is [autophagy's](http://autophagy.io/) bread diary. I am mostly
working from Rose Levy Beranbaum's [The Bread Bible](http://books.wwnorton.com/books/The-Bread-Bible/),
but will include other sources in the posts as I use them.

{% assign sorted_posts = (site.posts | sort: 'bread_num') | reverse %}
{% for post in sorted_posts %}
<h4>
  {% if post.bread_num %}
  <span class="bread-num">{{post.bread_num}}</span>
  {% endif %}
  <a href="{{BASE_PATH}}{{ post.url }}">{{post.title}}</a>
  <span class="post-date">/ {{post.datarum | autophagian_date}}</span>
</h4>
{% endfor %}
