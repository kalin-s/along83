a---
layout: default
title: Theoretically Hireable
---

{% assign all_essays = site.essays | sort: 'date' | reverse %}
{% for essay in all_essays %}
<article>
  <h2><a href="{{ essay.url | relative_url }}">{{ essay.title }}</a></h2>
  <p class="post-meta">{{ essay.date | date: "%B %-e, %Y" }}{% if essay.tags %} · {{ essay.tags | array_to_sentence_string }}{% endif %}</p>
  <p>{{ essay.excerpt }}</p>
</article>
<hr style="border:none; border-top:1px solid rgba(255,255,255,0.03); margin:1rem 0;">
{% endfor %}
