---
layout: home
title: Home
nav_order: 1
permalink: /
---

# Coding with AI
{: .fs-9 }

A collection of projects and AI-assisted coding sessions from my YouTube channel.
{: .fs-6 .fw-300 }

[Watch on YouTube](https://youtube.com/c/YOUR_CHANNEL){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }
[View on GitHub](https://github.com/randallard/coding-with-ai){: .btn .fs-5 .mb-4 .mb-md-0 }

---

## Projects

Browse through my AI-assisted coding projects and see how I use AI tools to build applications, solve problems, and learn new technologies.

{% assign sorted_pages = site.html_pages | sort: "nav_order" %}
{% assign project_pages = sorted_pages | where: "parent", nil | where_exp: "item", "item.title != 'Home'" %}

<div class="projects-grid">
{% for project in project_pages %}
  <div class="project-card">
    <h3><a href="{{ project.url | absolute_url }}">{{ project.title }}</a></h3>
    <p>{{ project.description }}</p>
    <span class="label">{{ project.technologies }}</span>
  </div>
{% endfor %}
</div>

## About This Site

This site contains all the projects and prompt examples from my "Coding with AI" YouTube channel, where I demonstrate how to leverage AI assistants like Claude, ChatGPT, and GitHub Copilot to enhance your coding workflow and build impressive projects.

Each project includes:
- Complete source code
- AI conversation logs showing the prompts used
- Step-by-step tutorials
- Lessons learned and best practices

Feel free to explore the projects, use the prompt examples for your own work, and adapt the techniques to your coding workflow!