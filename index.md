---
layout: default
title: House Recipes
pagination:
  enabled: true
  trail:
    before: 2 # The number of links before the current page
    after: 2  # The number of links after the current page
---

<div id="home">
<h1> Recent </h1>
  {% for post in paginator.posts %}
	<h2>{{ post.title }}</h2>
	<p class="meta"><i>Post date</i>: {{ post.date | date_to_string }}</p>
	<div class="post">
	{{ post.content }}
	</div>
    <br><hr><br>
  {% endfor %}
  {% if paginator.page_trail %}
    <ul class="pager">
    {% for trail in paginator.page_trail %}
    <li {% if page.url == trail.path %}class="selected"{% endif %}>
        <a href="{{ trail.path | prepend: site.baseurl }}" title="{{trail.title}}">{{ trail.num }}</a>
    </li>
    {% endfor %}
    </ul>
  {% endif %}
</div>
