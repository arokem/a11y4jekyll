---
layout: page
title: Blog
permalink: /blog/
---

## All Blog Posts

{% if site.posts.size > 0 %}
<ul class="post-list">
  {% for post in site.posts %}
  <li class="post-list-item">
    <h2 class="post-list-title">
      <a href="{{ post.url | relative_url }}">
        {{ post.title | escape }}
      </a>
    </h2>
    <p class="post-meta">
      <time datetime="{{ post.date | date_to_xmlschema }}">
        {{ post.date | date: "%B %d, %Y" }}
      </time>
      {% if post.author %}
      by {{ post.author }}
      {% endif %}
    </p>
    {% if post.excerpt %}
    <div class="post-excerpt">
      {{ post.excerpt }}
    </div>
    {% endif %}
    {% if post.tags.size > 0 %}
    <p>
      <strong>Tags:</strong>
      {% for tag in post.tags %}
        <span class="tag">{{ tag }}</span>{% unless forloop.last %}, {% endunless %}
      {% endfor %}
    </p>
    {% endif %}
  </li>
  {% endfor %}
</ul>
{% else %}
<p>No posts published yet. Check back soon!</p>
{% endif %}
