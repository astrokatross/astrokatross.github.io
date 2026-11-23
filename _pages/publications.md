---
title: "Publications"
permalink: /publications/
layout: single
author_profile: true
classes: wide
---

{% assign publications = site.publications | sort: "date" | reverse %}

{% for post in publications %}

## {{ post.title }}

{% if post.excerpt %}
{{ post.excerpt }}
{% endif %}

{% if post.venue %}
**{{ post.venue }}**
{% endif %}

{% if post.date %}
{{ post.date | date: "%Y" }}
{% endif %}

[Read more]({{ post.url | relative_url }}){: .btn .btn--primary }

{% if post.paperurl %}
[View paper]({{ post.paperurl }}){: .btn .btn--inverse }
{% endif %}

---

{% endfor %}