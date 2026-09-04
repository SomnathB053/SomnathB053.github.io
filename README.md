A clean stripped down personal website project, customized from the [AcademicPages](https://github.com/academicpages/academicpages.github.io) template.

---

## Quickstart & Local Development

### Run Local Server using dev containers.

```bash
bundle exec jekyll serve -H 0.0.0.0 -w --config _config.yml,_config_docker.yml
```


## Content Collections

The project is streamlined around three primary content collections:

| Collection | Folder | Description |
| --- | --- | --- |
| **Projects** | `_projects/` | Robotics builds, software, and hardware write-ups. Rendered as elongated, unrounded horizontal cards. |
| **Publications** | `_publications/` | Conference papers, journal articles, and preprints. |
| **Logs** | `_logs/` | Engineering lab notes, hardware benchmarks, and setup logs. |

---

## Drafting & Hiding WIP Content

To keep unfinished drafts organized directly inside their target collection folders (`_projects/`, `_logs/`, or `_publications/`) without publishing them to the live site, use the `published` flag in the YAML front matter:

```yaml
---
title: "WIP Project Title"
published: false
---
```

Files with `published: false` remain in place but are omitted from production builds, archives, and taxonomy tags.

---

Here is the updated section with generic placeholder text and dummy metadata:

## Content Templates

### 1. Projects (`_projects/`)

Place markdown files in `_projects/`. Use `header.teaser` for the widescreen thumbnail on horizontal listing cards:

```yaml
---
title: "Project Alpha Title"
collection: projects
permalink: /projects/project-alpha/
excerpt: "A brief one- or two-sentence description of the project, problem statement, or outcome."
header:
  teaser: /images/500x300.png
tags:
  - placeholder-tag-1
  - placeholder-tag-2
---
```
Edit `_pages_/portfolio.html` for visuals.


### 2. Engineering Logs (`_logs/`)

Place markdown files in `_logs/`:

```yaml
---
title: "Log Entry Title / Topic"
date: 2026-01-01
collection: logs
permalink: /logs/log-entry-title/
excerpt: "Short summary of the debugging session, benchmark run, or setup notes."
tags:
  - debugging
  - notes
---
```
Edit `_pages_/logs.html` for visuals.


### 3. Publications (`_publications/`)

Place markdown files in `_publications/`:

```yaml
---
title: "Title of Paper or Publication"
collection: publications
permalink: /publications/paper-title/
date: 2026-01-01
venue: "Name of Conference or Journal"
paperurl: "[https://example.com/paper.pdf](https://example.com/paper.pdf)"
citation: "Author, A., Author, B. (2026). \"Title of Paper.\" Name of Conference/Journal."
---
```
Edit `_pages_/publications.html` for visuals.

## CV / Resume (`_data/cv.json`)

The CV page (`/cv/`) uses a custom single-column layout with a floating sticky table of contents (TOC) sidebar.

* **Data Source:** Edit `_data/cv.json` to update sections, education, experience, and contact details. Edit `_includes/cv-template.html` for visuals. 
* **PDF Download:** Place your compiled resume at `assets/cv.pdf` to link with the top-right download button.
---
