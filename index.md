---
layout: default
title: 31° n, 139° w
---

{% for essay in site.essays %}
<article>
  <h2><a href="{{ essay.url | relative_url }}">{{ essay.title }}</a></h2>
  {% if essay.date %}
    <p class="post-meta">{{ essay.date | date: "%B %-e, %Y" }}</p>
  {% endif %}

  <p>
    {{ essay.content | strip_html | truncate: 250 }}
    {% if essay.content | strip_html | size > 250 %}… <a href="{{ essay.url | relative_url }}">read more</a>{% endif %}
  </p>
</article>
{% endfor %}
