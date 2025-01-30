---
layout: page
title: projects
permalink: /projects/
description: A growing collection of our research projects.
nav: true
nav_order: 3
display_categories: [ongoing, finished]
horizontal: true

projects:
  - date: 2024.6 - 2027.5
    funding: 글로벌인문사회융합연구지원사업
    desc: 기업의 ESG 경영에 관한 연구-환경오염과 국민건강을 중심으로
    category: ongoing
  - date: 2024.1 - 2024.12
    funding: 환경부
    desc: 친환경-생분해 박테리오파지 나노구조 센서 기반 휴대용 토양오염물질 측정 IoT 디바이스 개발
    category: finished
  - date: 2024.2 - 2024.8
    funding: 네이버웹툰
    desc: 2023년 한국 창작 생태계 기여 효과
    category: finished
    extlink: https://webtoonscorp.com/ko/storiesDetail?seq=32014

vanished:
  - date: 2021.1 - 2021.9
    funding: 중소벤처기업부
    desc: 멀티 채널 데이터 기반의 점포 입지 DB구축 및 AI 기반 추천 솔루션
    category: finished
  - date: 2018.4 - 2018.6
    funding: (주)네이버
    desc: 한국 온라인 창업 성장 리포트-네이버 스마트스토어 사례 분석
    category: finished
  - date: 2015.1 - 2015.8
    funding: (주)네이버
    desc: 네이버 포털 서비스 빅데이터 처리 요소 기술 개발
    category: finished
  - date: 2014.9 - 2015.8
    funding: 미래창조과학부
    desc: 확장된 우도 예측법과 고차원 데이터 분석
    category: finished
  - date: 2014.9 - 2015.8
    funding: 서울대학교 데이터과학과 지식창출 연구센터
    desc: SRC-STAT 국산 통계 패키지 개발
    category: finished
  - date: 2012.3 - 2013.2
    funding: 교육과학기술부
    desc: 심층 정보검색 기술 연구와 웹 마이닝
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
              <span class="badge font-weight-bold text-uppercase align-middle project-{{ category }}" style="min-width: 75px">{{ project.date }}</span>
            </div>
            <div class="col-xs-10 cl-sm-10 col-md-10 mt-2 mt-md-0">
              <h6 class="title font-weight-bold ml-1 ml-md-4 noto-sans-kr">{{ project.funding }}</h6>
              <h6 class="ml-1 ml-md-4 noto-sans-kr" style="font-size: 0.95rem;">{{ project.desc }}
                {% if project.extlink %}
                  <a href="{{ project.extlink }}"><i class="fa-solid fa-link"></i></a>
                {% endif %}
              </h6>
            </div>
          </div>
        </li>
      </ul>
    {% endfor %}
  {% endfor %}
</div>
