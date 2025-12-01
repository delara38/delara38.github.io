---
layout: page
permalink: /repositories/
title: Repositories
description: Brief overview of github profile
nav: true
nav_order: 4
---

## GitHub Profile

<p>
  <a href="https://github.com/delara38" target="_blank" rel="noopener noreferrer">
    <i class="fa-brands fa-github"></i> delara38
  </a>
</p>

---

## Repositories

<div class="repo-list">
  {% for repo in site.data.repositories.github_repos %}
    {% assign repo_parts = repo | split: '/' %}
    {% assign repo_name = repo_parts[1] %}
    <div class="repo-card p-3 mb-3" style="border: 1px solid var(--global-divider-color); border-radius: 8px;">
      <h5 style="margin-bottom: 0.5rem;">
        <a href="https://github.com/{{ repo }}" target="_blank" rel="noopener noreferrer">
          <i class="fa-brands fa-github"></i> {{ repo_name | replace: '_', ' ' | replace: '-', ' ' }}
        </a>
      </h5>
      <p class="text-muted mb-0" style="font-size: 0.9rem;">
        <code>{{ repo }}</code>
      </p>
    </div>
  {% endfor %}
</div>
