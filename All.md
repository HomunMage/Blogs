---
layout: base
---

<main class="post-content">
  <h2>Articles：</h2>
  <ul>
  {% assign filtered_pages = site.pages %}  
  {% assign sorted_pages = filtered_pages | sort: 'date' | reverse %}
  {% for p in sorted_pages %}
      <li>
        <a style="font-size: 2em;" href="{{ p.url | relative_url }}">{{ p.title }}</a>
        {{ p.date | date: "%B %d, %Y" }}
        <div>{{ p.content | markdownify }}</div>
      </li>
  {% endfor %}
  </ul>
</main>
