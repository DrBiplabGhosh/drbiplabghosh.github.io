---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}

You can find the complete publication list on <a href="https://scholar.google.com/citations?hl=en&user=-twoGx8AAAAJ">
<span style="color:gray">my Google Scholar profile</span></a>.


<ul>
{% for post in site.publications reversed %}

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


#<h2><span style="color:gray"> Bookchapters </span></h2>
#{% for post in site.bookchapters reversed %}
#  {% include archive-single-pub.html %}
#{% endfor %}
