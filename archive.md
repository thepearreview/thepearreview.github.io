---
layout: archive
title: Archive
---

<h1>All Episodes</h1>

{%-include post_list.html category=page.which_category-%}

<h1> Episodes by Category </h1>

{% assign items_grouped = site.posts | group_by: 'category' %}
{% for group in items_grouped %}

## {{group.name}}

{% for item in group.items %}

* [{{item.title}}]({{ item.url }})

{% endfor %}

{% endfor %}
