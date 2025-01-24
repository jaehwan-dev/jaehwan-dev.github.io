---
layout: page
title: projects
permalink: /projects/
description: A growing collection of your cool projects.
nav: true
nav_order: 3
display_categories: [ongoing, finished]
horizontal: true

projects:
  - date: 2026 - 2027
    funding: 한국연구재단
    desc: ESG를 활용한 어쩌고 저쩌고
    category: ongoing
  - date: 2021
    funding: 벤처창업부
    desc: 새로운 소식이 있나요
    category: finished
  - date: 2021
    funding: 벤처창업부
    desc: 새로운 소식이 있나요
    category: finished
---

<!-- pages/projects.md -->
<div class="projects">
  {% for category in page.display_categories %}
    <a id="{{ category }}" href=".#{{ category }}">
      <h2 class="category">{{ category }}</h2>
    </a>
    {% assign categorized_projects = page.projects | where: "category", category %}
    {% for project in categorized_projects %}
      <ul class="card-text font-weight-light list-group list-group-flush">
        <li class="list-group-item">
          <div class="row">
            <div class="col-xs-2 cl-sm-2 col-md-2 text-center date-column">
              <span class="badge font-weight-bold danger-color-dark text-uppercase align-middle" style="min-width: 75px">{{ project.date }}</span>
            </div>
            <div class="col-xs-10 cl-sm-10 col-md-10 mt-2 mt-md-0">
              <h6 class="title font-weight-bold ml-1 ml-md-4 noto-sans-kr">{{ project.funding }}</h6>
              <h6 class="ml-1 ml-md-4 noto-sans-kr" style="font-size: 0.95rem;">{{ project.desc }}</h6>
            </div>
          </div>
        </li>
      </ul>
    {% endfor %}
  {% endfor %}
</div>
