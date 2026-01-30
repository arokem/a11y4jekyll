---
layout: default
title: Home
---

<section class="home">
  <h1>Welcome to the Accessible Jekyll Template</h1>
  
  <p>This is a fully accessible Jekyll website template that complies with <strong>WCAG 2.1 Level AA</strong> standards and <strong>Title II</strong> requirements of the Americans with Disabilities Act.</p>
  
  <h2>Key Accessibility Features</h2>
  
  <ul>
    <li><strong>Semantic HTML5:</strong> Proper use of header, nav, main, footer, article, and other semantic elements</li>
    <li><strong>ARIA Landmarks:</strong> Clear navigation with role attributes and aria-labels</li>
    <li><strong>Keyboard Navigation:</strong> All interactive elements are keyboard accessible with visible focus indicators</li>
    <li><strong>Skip Navigation:</strong> Skip to main content link for keyboard users</li>
    <li><strong>Color Contrast:</strong> All text has at least 4.5:1 contrast ratio (WCAG AA compliant)</li>
    <li><strong>Responsive Design:</strong> Mobile-friendly and works on all screen sizes</li>
    <li><strong>Screen Reader Friendly:</strong> Proper heading hierarchy and descriptive labels</li>
    <li><strong>Focus Management:</strong> Clear focus indicators for keyboard navigation</li>
    <li><strong>Alternative Text:</strong> All images require alt text</li>
    <li><strong>Reduced Motion Support:</strong> Respects user's motion preferences</li>
  </ul>
  
  <h2>Recent Blog Posts</h2>
  
  {% if site.posts.size > 0 %}
  <ul class="post-list">
    {% for post in site.posts limit:5 %}
    <li class="post-list-item">
      <h3 class="post-list-title">
        <a href="{{ post.url | relative_url }}">
          {{ post.title | escape }}
        </a>
      </h3>
      <p class="post-meta">
        <time datetime="{{ post.date | date_to_xmlschema }}">
          {{ post.date | date: "%B %d, %Y" }}
        </time>
      </p>
      {% if post.excerpt %}
      <p>{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
      {% endif %}
    </li>
    {% endfor %}
  </ul>
  <p><a href="{{ '/blog/' | relative_url }}">View all posts &rarr;</a></p>
  {% else %}
  <p>No posts yet. Check back soon!</p>
  {% endif %}
  
  <h2>Getting Started</h2>
  
  <p>To use this template:</p>
  
  <ol>
    <li>Clone this repository</li>
    <li>Install Jekyll and dependencies: <code>bundle install</code></li>
    <li>Run the development server: <code>bundle exec jekyll serve</code></li>
    <li>Customize the content and styles to match your needs</li>
  </ol>
  
  <p>For more information about accessibility, visit the <a href="https://www.w3.org/WAI/">Web Accessibility Initiative (WAI)</a>.</p>
</section>
