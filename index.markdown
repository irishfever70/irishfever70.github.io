---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---


{% assign date = '2020-04-13T10:20:00Z' %}

Un petit test de build avec un plugin
- Original date - {{ date }}
- with timeago filter - {{ date | timeago }}
