---
layout: page 
title: Search 
permalink: /search/
main_nav: true
order: 2
---

<!--
-->
<div class="search-bar">
  <i class="fa fa-search" aria-hidden="true"></i>
  <input id="search-input" type="text" placeholder="Search..." />
</div>
<ul id="results-container"></ul>
  
<!--
<article class="post-content">
  <ul class="posts-list">
    {% for post in site.posts %}
    <li>
      <strong><a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></strong>
      <span class="post-date"> - {{ post.date | date: "%B %-d, %Y" }}</span>

      <br>
      {% if post.tags.size > 0 %}
        <i class="fa fa-tag fa-fw" style="color: rgb(150, 150, 150);"></i>
        {% for tag in post.tags %}
          <span class="tags">{{ tag }}</span>
          {% if forloop.last == false %}, {% endif %}
        {% endfor %}
      {% endif %}
    </li>
    {% endfor %}
  </ul>
</article>
-->

<!-- Script pointing to jekyll-search.js -->
<script src="/js/simple-jekyll-search.js" type="text/javascript"></script>

<script type="text/javascript">
SimpleJekyllSearch({
     searchInput: document.getElementById('search-input'),
     resultsContainer: document.getElementById('results-container'),
     json: '/search.json',
     searchResultTemplate: '<li>\
      <div>\
      <i class="fa fa-folder fa-fw" style="color: rgb(150, 150, 150);"></i> <a href="{url}"> {categories} / \
      <i class="fa fa-book fa-fw" style="color: rgb(150, 150, 150);"></i> {title} / \
      <i class="fa fa-calendar fa-fw" style="color: rgb(150, 150, 150);"></i> {date} \
      <br>\
      <i class="fa fa-tag fa-fw" style="color: rgb(150, 150, 150);"></i> {no tags} </a> \
      </div>\
      </li>',
     noResultsText: 'No results found',
     limit: 15,
     fuzzy: false,
     exclude: ['Welcome']
});
</script>