---
layout: default
title: Journal
permalink: /journal
---

# Journal

{% assign entries = site.journal | sort: "date" | reverse %}
{% for e in entries %}
- [{{ e.title }}]({{ e.url | relative_url }}) — {{ e.date | date: "%b %-d, %Y" }}
{% endfor %}
