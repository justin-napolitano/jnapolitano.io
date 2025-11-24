---
slug: github-jnapolitano-io-writing-overview
id: github-jnapolitano-io-writing-overview
title: 'jnapolitano.io: My Static Site Automation Toolkit'
repo: justin-napolitano/jnapolitano.io
githubUrl: https://github.com/justin-napolitano/jnapolitano.io
generatedAt: '2025-11-24T17:35:37.636Z'
source: github-auto
summary: >-
  I created the jnapolitano.io repo to simplify my experience in building and
  maintaining a static website. It merges deployment automation with backup
  solutions, plus a sprinkle of LaTeX for good measure. Here's a breakdown of
  what this thing is all about.
tags: []
seoPrimaryKeyword: ''
seoSecondaryKeywords: []
seoOptimized: false
topicFamily: null
topicFamilyConfidence: null
kind: writing
entryLayout: writing
showInProjects: false
showInNotes: false
showInWriting: true
showInLogs: false
---

I created the jnapolitano.io repo to simplify my experience in building and maintaining a static website. It merges deployment automation with backup solutions, plus a sprinkle of LaTeX for good measure. Here's a breakdown of what this thing is all about.

## Why This Repo Exists

Managing a static site can be tedious. I wanted a solution that allowed me to handle deployments, backups, and even have a professional-looking resume at my fingertips—without the hassle. This repo automates a bunch of workflows I was doing manually, which means less time fiddling with scripts and more time focusing on content.

## Key Design Decisions

The main goal was to create a one-stop shop for automating site management while keeping it extensible. Here’s how I approached it:

### Simple Automation

- **Deployment Scripts**: Why not let scripts do the heavy lifting? I used shell scripts to handle the deployment to GitHub Pages seamlessly.
- **Backup Solutions**: The site generates valuable content, and I needed a robust way to back it up. Enter the Dropbox API—easy to set up and works like a charm.

### Flexibility with Tech Stack

- **Python and Bash**: I lean on Python for the heavy lifting, especially for backups and builds. Bash scripts tie everything together, making setup a breeze.
- **LaTeX**: I’m a fan of well-formatted documents. The LaTeX templates make it easy to customize and generate my resume.

## Tech Stack

Here's what I'm using under the hood:

- **JavaScript**: Powers any front-end dynamics (mostly just the website’s interactivity).
- **Python 3.5+**: Ideal for scripting those backups and build tasks.
- **Bash**: Great for deployment and setup automation.
- **Makefile**: Clean way to automate the build process.
- **Docker**: Helps in getting my environment just right without conflicts.
- **Dropbox API**: For handling backups.
- **LaTeX**: For generating my resume in PDF format.

## Key Features

To put it simply, here’s what you can do with this repo:

- Automate deployments with shell scripts.
- Backup your site to Dropbox.
- Build the site using Python and Makefile.
- Use LaTeX templates for resumes.
- Get your environment set up with Docker.

## Getting Started

### Prerequisites

You’ll need a few things to get going:

- Python 3.5 or higher
- pip for managing Python packages
- A Dropbox account with an API token
- Make utility
- Git for version control

### Installation Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/justin-napolitano/jnapolitano.io.git
   cd jnapolitano.io
   ```

2. Install required Python dependencies:
   ```bash
   pip install -r requirements.txt
   ```

### How to Use

- **Build the site**: 
  ```bash
  make html
  ```
- **Deploy to GitHub Pages**:
  ```bash
  ./deploy.sh
  ```
- **Backup the built HTML to Dropbox**:
  ```bash
  python backup_html.py
  ```
- **Set up your environment**:
  ```bash
  ./install.sh
  ```
- **Clean up or uninstall**:
  ```bash
  ./uninstall.sh
  ```

## Project Structure

Here’s a quick breakdown of the major components in the project:

```
acp.sh            # Assumed automation script
backup_html.py    # Backup script for sending files to Dropbox
chtml.sh          # HTML processing script
deploy.sh         # Deploys the site to GitHub Pages
deployz.sh        # Alternative deploy script
Dockerfile        # For setting up the Docker environment
latex/            # Contains LaTeX templates
Makefile          # Build automation rules
requirements.txt  # Python package dependencies
source/           # Documentation source code
README.md         # This file
```

## Future Work / Roadmap

What’s next? There’s always room for improvement:

- **Script Documentation**: I want to document shell scripts better. Using a command should be intuitive.
- **Backup Enhancements**: I’ll add error handling and token management to the backup script. Keeping data safe is crucial.
- **Unit Tests**: Unit tests will be a focus for the Python scripts. You can't trust your code without them.
- **Docker Improvements**: I want full environment reproducibility with the Docker setup.
- **Better LaTeX Templates**: More options for resume customization are definitely on my radar.
- **CI/CD Integration**: Automated testing and deployment is the dream. Time to make it a reality.

## Wrap Up

In the end, jnapolitano.io is more than a collection of scripts. It’s a toolkit that makes managing a static site less of a hassle while also supporting my resume needs. If you're interested in updates or want to see how this evolves, catch me on Mastodon, Bluesky, or Twitter. 

Feel free to give it a try! I’m always open to feedback or contributions.
