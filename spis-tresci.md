---
layout: Post
title: Spis treści
permalink: /spis/
content-type: eg
---

Strona jest eksperymentem łączącym elementy podręcznika do ekonomii z koncepcją _digital garden_.

Lekturę można rozpocząć od dowolnego tagu lub według spisu.

[[Wzrost gospodarczy::/tags/#Wzrost-gospodarczy]]

<br>
<div>
{% for tag in site.tags %}
  {%- assign conc = tag | first -%}
  {%- if conc != 'Favorite' -%}
    <h2 id="{{ conc }}">{{ conc }}</h2>
    {% for post in tag.last %} 
      <li id="category-content" style="padding-bottom: 0.6em; list-style: none;"><a href="{{post.url}}">{{ post.title }}</a></li>
    {% endfor %}
  {%- endif -%}
{% endfor %}
</div>
<br/>




