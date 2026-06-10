---
layout: default
---
<article class="blog-wrap">
  <a class="post-back" href="{{ '/blog/' | relative_url }}">← All Posts</a>
  <div class="post-meta">{{ page.date | date: "%b %-d, %Y" }}{% if page.author %} · {{ page.author }}{% endif %}</div>
  <h1 class="post-title">{{ page.title }}</h1>
  {% if page.subtitle %}<p class="post-sub">{{ page.subtitle }}</p>{% endif %}
  <div class="post-body" style="margin-top:36px">
    {{ content }}
  </div>
  <div class="post-foot">
    <a class="btn btn-gold" href="{{ '/#contact' }}">Book a Demo</a>
    <a class="btn btn-navy" href="{{ '/blog/' | relative_url }}">More Articles</a>
  </div>
</article>
