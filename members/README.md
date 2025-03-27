# Team Members Directory

This directory contains profile information for team members that are displayed on the "About" page of the CLS Foundation website.

## Adding a New Member

To add a new team member, create a new `.qmd` file with the member's name (e.g., `jane-smith.qmd`). Each file should have the following structure:

```yaml
---
title: "Full Name"
position: "Job Title"
email: "email@example.com"
twitter: "@twitterhandle"  # Optional
github: "githubusername"   # Optional
image: "/assets/members/filename.jpg"  # Path to profile image
order: 4  # Controls display order (lower numbers appear first)
description: "A brief single-paragraph description that will appear in the member card."
---

Bio paragraph goes here. This should be 2-3 sentences about the person's 
background and experience.

A second paragraph can be added for additional information if needed.
```

## Profile Images

Profile images should be:
- Square format (1:1 aspect ratio)
- At least 300x300 pixels (larger is better)
- Placed in the `/assets/members/` directory
- Professional headshots are preferred

## Ordering

The `order` field in the YAML front matter controls the display order of team members on the About page. Lower numbers appear first.

## Social Media Links

The following social media links are supported:
- Email (required)
- Twitter (optional)
- GitHub (optional)

To add support for additional social media platforms, edit the EJS template in `views/members-grid.ejs`. 