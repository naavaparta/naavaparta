---
layout: page
title: Archive
---

This list includes my notes that I have so far written and published.

The <b>Seedling</b> notes are mere notes of someone else's content, they do not have any original thought behind them. They're oftentimes poorly connected, if at all, and they generally lack any kind of structure.

The <b>Budding</b> notes have a little bit of my own thought. They might even have some originality, sometimes they're connected well, sometimes poorly, but oftentimes they do have a structure of some kind.

The <b>Evergreen</b> notes are well-structured, complete with original thoughts and connections, and they will usually have a structure. They're almost <em>blog-worthy</em>, but as I don't blog, they're not going to be blog texts.

## The Notes

<ul class="archive">
{% for note in site.notes %}
<li><a href="{{ note.url }}{%- if site.use_html_extension -%}.html{%- endif -%}" class="internal-link">{{note.title}}</a>{% if note.category != null %}, a {{note.category}} note{% endif %} <span>({{ note.last_modified_at | date: "%B %Y" }})</span><p>{{ note.excerpt | strip_html | truncate: 200, "..." }}</p></li>
{% endfor %}
</ul>
