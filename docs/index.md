---
layout: default
---

### Documentation

Welcome to the documentation site. Contact the maintainers at: [{{ site.author }}]({{ site.email }})

#### Directories

{% assign tools = site.static_files | where:"extname",".md" | map:"path" | uniq %}

{% for tool in tools %}
* {{ tool }}
{% endfor %}

#### Test2

{% assign dirs = site.pages | where_exp:"item","item.path contains '.md'" | map:"dir" | uniq %}

{% for dir in dirs %}
* {{ dir }}
{% endfor %}
