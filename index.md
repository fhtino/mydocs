---
layout: default
---

Welcome to my personal docs website about coding, cloud, sql, windows, linux and so on. Feel free to send me your feedback. It is always appreciated.

<br/>
 

 
{% assign sorted_pages = site.pages | where:"listing","1" | sort:"publish_date" | reverse %}

{% for p in sorted_pages %}   
  <div style="margin-top:10px;">
    <div style="font-size:larger;"><a href="{{ p.url }}">{{p.title}}</a></div>
    <div style="font-size:smallerxxxx; font-style:italic;">{{p.abstract}}</div>
    <div style="font-size:smaller">{{p.publish_date}}</div>
  </div>    
{% endfor %}
 
