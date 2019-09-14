---
layout: page
title: Teaching
permalink: /teaching/
description: Some courses I taught/tutored.
---

{% for teaching in site.teachings %}

{% if teaching.redirect %}
<div class="teaching">
    <div class="thumbnail">
        <a href="{{ teaching.redirect }}" target="_blank">
         <span>
            <h1>{{ teaching.title }}</h1>
            <br/>
            <p>{{ teaching.description }}</p>
        </span>
        {% if teaching.img %}
        <img class="thumbnail" src="{{ teaching.img | prepend: site.baseurl | prepend: site.url }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        </a>
    </div>
</div>
{% else %}

<div class="teaching ">
    <div class="thumbnail">
        <a href="{{ teaching.url | prepend: site.baseurl | prepend: site.url }}">
        <span>
            <h1>{{ teaching.title }}</h1>
            <br/>
            <p>{{ teaching.description }}</p>
        </span>
        {% if teaching.img %}
        <img class="thumbnail" src="{{ teaching.img | prepend: site.baseurl | prepend: site.url }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        </a>
    </div>
</div>

{% endif %}

{% endfor %}
