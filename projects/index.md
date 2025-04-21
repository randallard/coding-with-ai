---
layout: default
title: Projects
nav_order: 2
description: Collection of AI-assisted coding projects
permalink: /projects/
has_children: true
---

# Projects

This section contains a collection of projects created with AI assistance. Each project includes source code, AI conversation logs, and detailed explanations of the development process.

## Available Projects

{% assign sorted_pages = site.html_pages | sort: "nav_order" %}
{% assign project_pages = sorted_pages | where: "parent", "Projects" %}

<div class="projects-grid">
{% for project in project_pages %}
  <div class="project-card">
    <h3><a href="{{ project.url | absolute_url }}">{{ project.title }}</a></h3>
    <p>{{ project.description }}</p>
    <span class="label">{{ project.technologies }}</span>
  </div>
{% endfor %}
</div>

### Featured Project

<div class="project-feature">
  <h3><a href="/coding-with-ai/projects/coding-with-ai/">Coding with AI</a></h3>
  <p>Sharing our experience learning to code with AI assistants and building this documentation site</p>
  <a href="/coding-with-ai/projects/coding-with-ai/" class="btn">View Project</a>
</div>

## Project Structure

Each project in this collection follows a consistent structure:

- Complete source code
- Step-by-step tutorials
- AI conversation logs showing the prompts used
- Lessons learned and best practices

Feel free to explore these projects and adapt the techniques to your own coding workflow!