---
layout: page
title: Resources
description: Helpful online resource
---

My own library of tools and resources that have helped me navigate startups, investing, personal development and more.

It brings me joy to be able to share, and have all of these resources in one place.

{% for category in site.data.resources %}
{% assign items = category[1] | sort_natural: "name" %}
### {{ category[0] | capitalize }}:
{% for item in items %}
* [{{ item.name }}]({{ item.link }}){:target="_blank"}
  * {{ item.description }}
{% endfor %}
{% endfor %}

---
