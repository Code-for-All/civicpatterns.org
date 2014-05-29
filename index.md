---
title: Civic Technology Design Patterns
layout: default
tagline: A design pattern language for technology that addresses social political and governance-related problems.
---

<ul>
    {% for page in site.pages %}{% if page.layout == 'pattern' %}
        <li>
            <a href="{{page.url}}"><strong>{{page.title}}</strong></a> {{page.tagline}}
        </li>
    {% endif %}{% endfor %}
</ul>
