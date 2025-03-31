# CLS Foundation Website Content Management Guide

## Overview

This website is built using [Quarto](https://quarto.org/), a markdown-based publishing system. Content is written in plain text files with simple formatting (markdown) that get converted to a fully-functioning website. The site automatically displays listings of programs, events, stories, and team members.

## Setup Your Work Environment

1. **Install Required Software:**
   - Install [R](https://cran.r-project.org/)
   - Install [Quarto](https://quarto.org/docs/get-started/)
   - Install [RStudio](https://posit.co/download/rstudio-desktop/)

2. **Get the Website Code:**
   - Clone this repository or download it to your computer
   - Open the project in RStudio by clicking on `cls-website.Rproj`

3. **Install R Dependencies:**
   - Open R console and run: `renv::restore()` 
   - This installs all required R packages based on the renv.lock file

## Understanding Markdown

The website content is written in Markdown - a simple markup language that's easy to learn:

- Basic formatting: **bold**, *italic*, [links](https://example.com)
- Lists (like this one)
- Headings (using # symbols)

Learn more: [Markdown Basics](https://quarto.org/docs/authoring/markdown-basics.html)

## Adding Content to the Website

The website automatically generates cards and pages for programs, events, stories, and team members using Quarto's "listing" feature. When you add a new file in the appropriate folder with the correct metadata, the website will:

1. Create a card for that item in the relevant listing page (e.g., programs.qmd)
2. Generate a dedicated page for the item with all its content
3. Include the item in listings on the homepage (if applicable)

No coding is required - just add your content files with the right metadata, and the website handles the rest.

### Programs

Create a new file in the `programs/` folder named `your-program-name.qmd` with this metadata at the top:

```
---
title: "Program Title"
description: "Brief description of the program"
image: "URL to program image"
category: "Program Category"
priority: 4  # Lower numbers appear first
url: "URL to more information" # or leave as "/programs/your-program-name"
---
```

Then add your content below using markdown.

### Events

Create a new file in the `events/` folder named `your-event-name.qmd` with this metadata:

```
---
title: "Event Title"
description: "Brief event description"
date: "YYYY-MM-DD"
end_date: "YYYY-MM-DD"  # Optional
image: "URL to event image"
location: "Event Location"
url: "URL for more info"  # Optional
categories: ["Category1", "Category2"]
---
```

### Success Stories

Create a new file in the `stories/` folder named `story-name.qmd` with this metadata:

```
---
title: "Story Title"
description: "Brief description"
client: "Client Name"
thumbnail: "URL to image"
date: "YYYY-MM-DD"
categories: ["Category1", "Category2"]
industry: "Industry Type"
---
```

### Team Members

Create a new file in the `members/` folder named `person-name.qmd` with this metadata:

```
---
title: "Person Name"
position: "Job Title"
email: "email@example.com"
image: "URL to profile image"
order: 3  # Lower numbers appear first
description: "Brief bio"
---
```

## Previewing and Publishing

### Render Website Locally

To preview changes before publishing:

1. Open terminal/command prompt in project folder
2. Run: `quarto preview` 
3. A browser will open showing the site
4. Changes to files will automatically refresh the preview

### Publish Changes

When you're satisfied with your changes:

1. Commit and push changes to the main branch
2. The website will automatically build and deploy

## Common Operations

- **Update existing content**: Edit the corresponding `.qmd` file
- **Remove content**: Delete the corresponding `.qmd` file
- **Change order**: Adjust the `priority` or `order` values in metadata
- **Update styling**: Contact the web developer for changes to visual design

## Need Help?

Refer to the [Quarto documentation](https://quarto.org/docs/guide/) for more details on markdown formatting and website features.