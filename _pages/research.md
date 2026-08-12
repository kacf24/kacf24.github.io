---
title: "Research"
layout: gridlay
sitemap: false
permalink: /research/
---

<style>
.research-row {
  display: flex;
  align-items: center;
  flex-wrap: wrap;
}

.research-img-container {
  text-align: center;
  padding: 15px;
}

.research-img-container img {
  width: 100%;
  max-width: 260px;
  height: auto;
  border-radius: 8px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.15);
}

.description-block {
  margin-top: 15px;
}
</style>

## Research
{% for topic in site.data.research %}
<div class="jumbotron">
<div class="row research-row">
<div class="col-sm-4 col-xs-12 research-img-container">
<img src="{{ site.url }}{{ site.baseurl }}/images/{{ topic.image }}" alt="{{ topic.name }}"/>
</div>
<div class="col-sm-8 col-xs-12">
<h1>{{ topic.name }}</h1>
<h5>Scale: {{ topic.region }}</h5>
<h6>Themes: {{ topic.topics }}</h6> 
<div class="description-block">
{{ topic.description | markdownify }}
</div>
</div>
</div>
</div>
{% endfor %}