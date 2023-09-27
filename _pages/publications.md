---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

<h2>Working Papers</h2>
{% for post in site.publications reversed %}
  {% if post.type == "jmp" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

{% for post in site.publications reversed %}
  {% if post.type == "wp" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

<h2>Book Chapters</h2>
{% for post in site.publications reversed %}
  {% if post.type == "book_chapter" %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}
