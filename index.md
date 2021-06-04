---
title: Инструкции в Интернете
permalink: index.html
layout: home
---

# Каталог содержимого

Гиперссылки на каждое пошаговое руководство. Инструкторы могут использовать пошаговое руководство в качестве демонстрации во время лабораторного занятия учащихся. 

## Пошаговые руководства

{% assign wts = site.pages | where_exp:"page", "page.url contains '/Instructions/Walkthroughs'" %}
| Модуль | Пошаговое руководство |
| --- | --- | 
{% for activity in wts %}| {{ activity.wts.module }} | [{{ activity.wts.title }}{% if activity.wts.type %} - {{ activity.wts.type }}{% endif %}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}

