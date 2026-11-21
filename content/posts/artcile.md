+++
title = "Verifying Local Builds Before Pushing to GitHub Pages"
date = 2026-11-20T12:00:00Z
draft = true
summary = "A quick checklist for catching broken links, draft flags, and layout issues locally before deploying with GitHub Actions."
tags = ["hugo", "workflow", "github-pages"]
ShowToc = true
+++

Before pushing new Markdown files to GitHub, running a quick local check saves you from waiting on a build or discovering broken pages after deployment. This short guide covers the basic checks to run every time you publish.

## 1. Check Front Matter and Draft Status

Make sure `draft` is set to `false` when a post is ready to publish, and give it a concise `summary` so your home feed and search index stay clean:

* Confirm `title` and `date` are accurate.
* Keep `summary` to one or two clear sentences.
* Add relevant `tags` so readers can group related posts.

## 2. Run the Local Preview Server

Start Hugo locally so you can inspect rendered HTML, navigation links, and your Table of Contents:

```bash
hugo server -D