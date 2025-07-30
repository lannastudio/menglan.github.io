---
layout: default
---
## 所有文章

<ul>
{% for post in site.posts %}
  <li>
    <a href="{{ post.url }}">{{ post.title }}</a>
    <span style="color:#999;">({{ post.date | date: "%Y-%m-%d" }})</span>
    {% if post.categories.size > 0 %}
      <span style="color:#bbb;">[分类: {{ post.categories | join: ", " }}]</span>
    {% endif %}
  </li>
{% endfor %}
</ul>
