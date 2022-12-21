---
layout: archive
title: "Oral Presentation"
permalink: /talks/
author_profile: true
---

{% include base_path %}

<ul>
{% for post in site.talks reversed %}

  {% assign currentdate = post.date | date: "%Y" %}
  {% if currentdate != date %}
    {% unless forloop.first %}</ul>{% endunless %}
    <h2 id="y{{post.date | date: "%Y"}}"><span style="color:gray">{{ currentdate }}</span></h2>
    <ul>
    {% assign date = currentdate %}
  {% endif %}
  {% if post.authors contains 'Biplab Ghosh' %}
    {% include archive-single-pub.html %}
  {% endif %}
  {% if forloop.last %}</ul>{% endif %}

{% endfor %}