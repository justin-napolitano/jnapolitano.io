---
slug: github-jnapolitano.io
title: Automating Static Site Management with jnapolitano.io
repo: justin-napolitano/jnapolitano.io
githubUrl: https://github.com/justin-napolitano/jnapolitano.io
generatedAt: '2025-11-23T09:11:21.259239Z'
source: github-auto
summary: >-
  Explore the automation of build, deployment, and backup processes for static
  sites using Python, shell scripts, and Dropbox integration.
tags:
  - static-site
  - github-pages
  - deployment
  - backup
  - python
  - automation
  - shell scripts
  - github pages
  - dropbox
  - sphinx
  - makefile
  - latex
  - docker
seoPrimaryKeyword: static site automation
seoSecondaryKeywords:
  - build pipeline automation
  - deployment scripts
  - backup solutions
  - LaTeX resume management
  - GitHub Pages deployment
seoOptimized: true
topicFamily: automation
topicFamilyConfidence: 0.9
topicFamilyNotes: >-
  The post focuses primarily on automating static site build, deployment, and
  backup using scripts and tooling like Makefiles, shell scripts, Python
  scripts, and API integrations. This matches closely the Automation family
  which includes build, deployment, git workflows, and content publishing
  automation.
kind: project
id: github-jnapolitano.io
---

# Technical Overview of jnapolitano.io

This repository is a multi-faceted project aimed at automating the build, deployment, and backup of a static site, as well as managing LaTeX resume templates. The core problem addressed is streamlining the workflow from source content to live deployment and ensuring data safety through backups.

## Motivation

Managing static sites often involves repetitive manual steps: building HTML, deploying to hosting platforms, and backing up generated content. This project automates these steps using a combination of shell scripts, Python scripts, and Makefiles. Additionally, it integrates Dropbox API for offsite backups, reducing the risk of data loss.

## Architecture and Components

### Build Pipeline

The build process is orchestrated primarily via `python_build.py` and a `Makefile`. The Python script encapsulates dependency installation (`pip install -r requirements.txt`), cleaning previous builds (`make clean`), building HTML documentation (`make html`), and git operations like add, commit, and push. The use of subprocess calls indicates reliance on external tools (make, git) rather than pure Python implementations.

### Deployment

Deployment is handled by shell scripts such as `deploy.sh` and `deployz.sh`. The `deploy.sh` script uses `ghp-import` to push the built HTML content to a GitHub Pages branch, enabling easy hosting at `cv.jnapolitano.io`. This method leverages GitHub's built-in static site hosting capabilities.

### Backup

The `backup_html.py` script uses the Dropbox Python SDK to upload the built HTML directory to a specified Dropbox path. It requires a Dropbox access token, which must be manually inserted. The script handles API errors, including insufficient space, and provides console feedback during uploads.

### Documentation

The `source/` directory contains Sphinx documentation configuration (`conf.py`) and source files. Extensions like `myst_nb`, `sphinx_copybutton`, and others suggest support for Markdown notebooks and enhanced documentation features.

### LaTeX Resume

The `latex/` directory holds LaTeX templates for a resume. The README hints at a single-page, one-column resume designed for software developers, emphasizing ease of use and consistent formatting.

## Implementation Details

- The project uses Python 3.5+ due to Dropbox SDK compatibility.
- Shell scripts automate common tasks like deployment, installation, and maintenance.
- The build pipeline is modularized into classes for configuration, dependency management, and build steps.
- Error handling in backup scripts is explicit, checking for API-specific errors.
- The deployment script uses `ghp-import` with flags to force push and set a custom domain.
- The project includes a Dockerfile, presumably to containerize the environment for consistent builds, though details are not fully visible.

## Practical Considerations

- The Dropbox token is hardcoded as a placeholder; secure token management is necessary for production use.
- The presence of both `requirements.txt` and a misspelled `requirments.txt` suggests cleanup is needed.
- Some scripts (`label_list.py`) interact with pickle files related to Sphinx build environments, indicating advanced documentation handling.
- Multiple shell scripts with overlapping names (`deploy.sh`, `deployz.sh`, `doit.sh`) imply iterative development or experimentation.

## Summary

This repository exemplifies a pragmatic approach to managing static site workflows and resume document generation. It combines scripting, API integration, and build automation to reduce manual overhead. Returning to this project, one should first ensure environment setup (Python, pip, Dropbox token), then follow the build and deployment scripts to maintain or extend the site and resume content.

Future improvements should focus on code cleanup, enhanced documentation, and secure credential handling to improve maintainability and security.

