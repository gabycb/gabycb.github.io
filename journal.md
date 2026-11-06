---
layout: default
title: Journal
permalink: /journal
---
<div class="about-content" markdown="1">

# Journal

{% assign entries = site.journal | sort: "date" | reverse %}
{% for e in entries %}
- [{{ e.title }}]({{ e.url | relative_url }}) — {{ e.date | date: "%b %-d, %Y" }}
{% endfor %}
