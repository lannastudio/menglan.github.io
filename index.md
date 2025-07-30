---
layout: default
---

## 欢迎👏👏👏👏

{% assign categories = site.categories | sort %}
<ul>
  {% for category in categories %}
    <li>
      <b>{{ category[0] }}</b>
      <ul>
        {% for post in category[1] %}
          <li>
          <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
            <span style="color:#999;">({{ post.date | date: "%Y-%m-%d" }})</span>
          </li>
        {% endfor %}
      </ul>
    </li>
  {% endfor %}
</ul>
