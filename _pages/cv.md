---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======

* Ph.D. student, School of Integrated Circuits, Southeast University, 2026-present

Research Interests
======

* Computer architecture
* CPU microarchitecture
* Cache optimization
* SoC Hardware/software co-design

Skills
======

* Programming: C/C++, Python, Shell
* Tools: Linux, Git, architecture simulation and profiling workflows
* Writing: Markdown, LaTeX, technical documentation

Projects
======

<ul>{% for post in site.portfolio %}
  {% include archive-single-cv.html %}
{% endfor %}</ul>
