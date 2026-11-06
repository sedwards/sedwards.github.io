---
layout: page
title: Downloads and source code
description: Find Updatez.org software and project source code.
---

Purchases help fund continued development. For help accessing a purchased package, contact [stevenaedwards82@gmail.com](mailto:stevenaedwards82@gmail.com).

## MacDependency

[Download MacDependency]({{ '/releases/MacDependency.dmg' | relative_url }}) · [View source on GitHub](https://github.com/sedwards/macdependency)

## More projects

Browse each repository for source code and build instructions:

{% for project in site.data.projects %}
* [{{ project.name }} on GitHub](https://github.com/{{ site.author.github }}/{{ project.repository }})
{% endfor %}

[Browse software and purchase options]({{ '/' | relative_url }}#software)
