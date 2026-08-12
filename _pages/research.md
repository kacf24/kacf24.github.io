---
title: "Research"
layout: gridlay
sitemap: false
permalink: /research/
---

<style>
img{
  border-radius: 1px;
}
.col-sm-4{
  margin-top:70px;
}
.col-md-3 {
  margin-top:5px;
  margin-bottom:5px;
  padding:0px;
  display:block;
  overflow:hidden;
  text-align:center;
  display: table-cell;
  background: white;
  border-radius: 20px;
  height: auto;
}
iframe {
  margin:0;
  padding:0;
  width: 175px;
  display: inline;
  vertical-align: middle;
}
</style>

## Research
{% for topic in site.data.research %}
<div class="jumbotron">
<div class="row">
<div class="col-sm-4">
  <img src="{{ site.url }}{{ site.baseurl }}/images/{{ topic.image }}" width="110%" style="max-width:250px"/>
</div>
<div class="col-sm-8 col-xs-12">
  <h1>{{ topic.name }}</h1>
  <h5>Scale: {{topic.region}}</h5>
  <h6>Themes: {{topic.topics}}</h6> 
  <div class="description-block">
  <strong>Description:</strong>
  {{ topic.description | markdownify }}
</div>

</div>
</div>
</div>
{% endfor %}