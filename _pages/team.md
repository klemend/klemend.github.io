---
title: "LEP - Člani"
layout: gridlay
excerpt: "LEP - Člani"
sitemap: false
permalink: /team/
---

# Člani laboratorija
(S klikom na ime izveste več)


---

## Predstojnik laboratorija
{% assign number_printed = 0 %}
{% for member in site.data.team_members %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if member.group == 0 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4><a href="{{ member.url | append: '.html'}}" class="off">{{ member.name }}</a></h4>
  <i>{{ member.info }}</i>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

---

## Člani
{% assign number_printed = 0 %}
{% for member in site.data.team_members %}

{% assign even_odd = number_printed | modulo: 3 %}
{% if member.group == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-4 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4><a href="{{ member.url | append: '.html' }}" class="off">{{ member.name }}</a></h4>
  <i>{{ member.info }}</i>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 2 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 3 %}
{% if even_odd != 0 %}
</div>
{% endif %}


<!---
---
## Administracija in alumni

{% for member in site.data.team_members %}
{% if member.group == 8 %}

<i class="alumni1">{{ member.name }}</i><br>
<i class="alumni2">{{ member.info }} ({{ member.year }}</i>) {% if member.current %} 
<i class="alumni2">Current: {{ member.current }}</i> {% if member.extlink %} <a class="alumni2" style="padding-left: 0px;" href="{{ member.extlink }}">(Link)</a>
{% endif %}
{% endif %}

{% endif %}
{% endfor %}
-->








