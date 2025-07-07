---
layout: page
title: Blog
icon: fas fa-blog
order: 4
permalink: /blog/
---

{% assign blog_posts = site.posts | where_exp: "post", "post.categories contains 'Blog'" %}

<ul>
  {% for post in blog_posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a> - {{ post.date | date: "%Y-%m-%d" }}
    </li>
  {% endfor %}
</ul>
