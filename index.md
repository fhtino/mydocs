---
layout: default
---

************ DRAFT ************ 

Welcome to my personal docs website about coding, cloud, sql, windows, linux and so on. Feel free to send me your feedback. It is always appreciated.

<br/>

[dfdsf](docs/test1)

 {% link docs/test1.md %}

 <hr/>

 
{% assign sorted_pages = site.pages | sort:"publish_date" | reverse %}

{% for p in sorted_pages %}   
{% if p.url contains "/docs/" %}
 
  

  <div style="margin-top:5px;">
    <div style="font-size:larger;"><a href="{{ p.url }}">{{p.title}}</a></div>
    <div style="font-size:smaller">&nbsp; &nbsp; {{p.publish_date}}</div>
  </div>
     
{% endif %}
{% endfor %}
 
