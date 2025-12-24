---
layout: page
title: News Categories
permalink: /categories/
---

# Browse by Topic

Explore our coverage by choosing a category below:

{% for category in site.categories %}
  <h2 id="{{ category | first | slugize }}">{{ category | first }}</h2>
  <ul>
    {% for post in category.last %}
      <li>
        <a href="{{ post.url }}">{{ post.title }}</a> 
        <small>({{ post.date | date: "%b %d, %Y" }})</small>
      </li>
    {% endfor %}
  </ul>
{% endfor %}
