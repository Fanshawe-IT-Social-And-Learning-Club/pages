---
layout: post
title: How to Maintain This Website
date: 2024-05-28 17:45:14 −0500
categories: How-To Jekyll
tags: how-to jekyll github-page
author: Colgrave34
pin: true
---
## Welcome!
Hi, to whom is reading this post, I'm glad and welcoming you to want to maintain this website.  
This document links to most of the stuff about how this website works, built and how to keep it working. I can't cover every single details, if you have a question, just ask me on Discord.

This is website is built with:
- [GitHub Page](https://pages.github.com/)
- [Jekyll](https://jekyllrb.com/)
- [jekyll-theme-chirpy](https://github.com/cotes2020/jekyll-theme-chirpy)

## Documentation & Links
[GitHub Pages Quickstart](https://docs.github.com/en/pages/quickstart)  
[Jekyll Quickstart](https://jekyllrb.com/docs/)  
[Jekyll Structure](https://jekyllrb.com/docs/structure/)  
[jekyll-theme-chirpy Wiki](https://github.com/cotes2020/jekyll-theme-chirpy/wiki)  
[chirpy-starter](https://github.com/cotes2020/chirpy-starter)  
[giscus](https://giscus.app/)  
[giscus config example](https://github.com/cotes2020/chirpy-starter/blob/main/_config.yml#L108)  

## GitHub Pages & Jekyll
If you don't know, GitHub Pages is a service provide for free to host static website built with Jekyll.  
Jekyll on the other hand is a static website generator, it has the ability to cover Markdown files to HTML. On top of that, Jekyll also have a ton of themes to choose from.  
This makes adding content dramatically easy with the help of git.

## Jekyll
For how to use Jekyll or local testing, please follow [How to contribute](/posts/how-to-contribute/).

## Theme
### Chirpy
We use Chirpy as our theme for easy spin up and... idk it just looks good.  
They recommend using [chirpy-starter](https://github.com/cotes2020/chirpy-starter), this is due to easy upgrade and it isolates irrelevant project files.

### Side Panel
All the tabs pages/permalink pages on the side panel are located in the `_tab` folder.

### Side Panel Button
I have made [a small modification](https://github.com/itslc2023/itslc2023.github.io/commit/b5813dc29e2efd3032ff0e69c0b5fb4f2330ad3f) to add a discord bottom to the sidebar, alongside the GitHub and Email button.  
This requires adding [Font Awesome](https://fontawesome.com/icons/discord?f=brands&s=solid) icon into the `_data/contact.yml` file, plus the link to discord. Additionally, adding just a blank config into the `_config.yml`.

### Favicon
[Chirpy Doc customize-the-favicon](https://chirpy.cotes.page/posts/customize-the-favicon/)

### Theme update
[Chirpy Doc Upgrade-Guide](https://github.com/cotes2020/jekyll-theme-chirpy/wiki/Upgrade-Guide)

### Changing the Theme
> Oh boy, what have we decide...

This is a daunting job. For changing the theme, I strongly recommend making a new branch and heavily testing it before merging. Beside Jekyll's directory structure, every theme's config and file structure is a bit different. Also, we need to move every post, assets, favicon, photos in to the new branch.  
Please follow the new theme's documentation for this.

## Custom Domain
Custom Domain is doable, but not implemented to our website at the moment.  
If we'd like in the future, purchase a domain and follow the documentation below.  
[GitHub Pages Doc custom-domain](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)

## Ruby Error
The website is automatically built with GitHub workflow and the `.yml` file is located at `.github/workflows/jekyll.yml`.  
Sometimes, after a Jekyll update, Rudy might also need an update in the workflow file, otherwise the build might fail.  
`line 39 .github/workflows/jekyll.yml`  
**This is only needed if the build failed, and it's specifically due to ruby version**  
**DO NOT CHANGE THE VERSION IF WE DON'T HAVE TO**

## At The End
Hey, thanks for reading this, I appreciate your contribution.  
If you think this doc needs work, feel free to contact me or make a PR, I'd happily update it.
