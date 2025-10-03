---
layout: page
title: About
description: About
keywords: SilverSpear1031
comments: true
menu: About
permalink: /about/
---

## Contact

<ul>
{% for website in site.data.social %}
  <li>
    {{ website.sitename }}：
    <a href="{{ website.url }}" target="_blank">
      {% if website.sitename == "Email" %}
        {{ website.name }}
      {% else %}
        @{{ website.name }}
      {% endif %}
    </a>
  </li>
{% endfor %}
</ul>


## Skill Keywords

{% for skill in site.data.skills %}
### {{ skill.name }}
<div class="btn-inline">
{% for keyword in skill.keywords %}
<button class="btn btn-outline" type="button">{{ keyword }}</button>
{% endfor %}
</div>
{% endfor %}



