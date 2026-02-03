---
layout: page
title: join us
permalink: /join_us/
description: Join our research team and contribute to cutting-edge projects.
nav: true
nav_order: 4
display_categories: [postdoc, phd, master, undergraduate]
horizontal: false
---

<!-- pages/join_us.md -->
<div class="join-us">
  {% if site.enable_join_categories and page.display_categories %}
    <!-- Display categorized positions -->
    {% for category in page.display_categories %}
      <a id="{{ category }}" href=".#{{ category }}">
        <h2 class="category">{{ category }}</h2>
      </a>
      
      {% assign categorized_positions = site.positions | where: "category", category %}
      {% assign sorted_positions = categorized_positions | sort: "importance" %}
      
      <!-- Generate cards for each position -->
      {% if page.horizontal %}
        <div class="container">
          <div class="row row-cols-1 row-cols-md-2">
            {% for position in sorted_positions %}
              {% include positions_horizontal.liquid %}
            {% endfor %}
          </div>
        </div>
      {% else %}
        <div class="row row-cols-1 row-cols-md-3">
          {% for position in sorted_positions %}
            {% include positions.liquid %}
          {% endfor %}
        </div>
      {% endif %}
    {% endfor %}
    
  {% else %}
    <!-- Display positions without categories -->
    {% assign sorted_positions = site.positions | sort: "importance" %}
    
    <!-- Generate cards for each position -->
    {% if page.horizontal %}
      <div class="container">
        <div class="row row-cols-1 row-cols-md-2">
          {% for position in sorted_positions %}
            {% include positions_horizontal.liquid %}
          {% endfor %}
        </div>
      </div>
    {% else %}
      <div class="row row-cols-1 row-cols-md-3">
        {% for position in sorted_positions %}
          {% include positions.liquid %}
        {% endfor %}
      </div>
    {% endif %}
  {% endif %}
</div>
