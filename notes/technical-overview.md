---
slug: github-jnapolitano-io-note-technical-overview
id: github-jnapolitano-io-note-technical-overview
title: jnapolitano.io Overview
repo: justin-napolitano/jnapolitano.io
githubUrl: https://github.com/justin-napolitano/jnapolitano.io
generatedAt: '2025-11-24T18:39:45.307Z'
source: github-auto
summary: >-
  This repo automates the building, deploying, and backing up of a static site
  at cv.jnapolitano.io, along with providing LaTeX resume templates. Here’s what
  you need to know:
tags: []
seoPrimaryKeyword: ''
seoSecondaryKeywords: []
seoOptimized: false
topicFamily: null
topicFamilyConfidence: null
kind: note
entryLayout: note
showInProjects: false
showInNotes: true
showInWriting: false
showInLogs: false
---

This repo automates the building, deploying, and backing up of a static site at cv.jnapolitano.io, along with providing LaTeX resume templates. Here’s what you need to know:

## Key Components
- **Scripts**: Handles deployment to GitHub Pages, Dropbox backups, and build pipelines using Python and Bash.
- **Tech Stack**: 
  - Python 3.5+
  - JavaScript
  - Bash
  - Docker
  - LaTeX
  
## Quick Start

1. Clone the repo:
   ```bash
   git clone https://github.com/justin-napolitano/jnapolitano.io.git
   cd jnapolitano.io
   ```
   
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Build the site:
   ```bash
   make html
   ```

4. Deploy:
   ```bash
   ./deploy.sh
   ```

## Gotchas
- You need a Dropbox API token for the backup script.
- Ensure you have Make installed for the build process.
