---
layout: default
title: House Recipes
---

# Recipes

## Cheeses

## Meat

## Pastry

## Quickbread

## Salads

## Sauces

<ul class="posts">
    {% for post in site.categories.sauces %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
</ul>
