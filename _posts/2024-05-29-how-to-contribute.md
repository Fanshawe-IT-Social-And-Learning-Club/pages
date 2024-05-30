---
layout: post
title: How to Contribute
date: 2024-05-29 17:12:33 −0500
categories: How-To Jekyll
tags: how-to jekyll github-page
author: Colgrave34
pin: true
---
## Welcome!
Hi, to whom is reading this post, I'm glad and welcoming you to want to maintain this website.  
This document links to most of the stuff about how this website works, built and how to keep it working. I can't cover every single details, if you have a question, just ask me on Discord.

## Documentation & Links
[Jekyll Quickstart](https://jekyllrb.com/docs/)  
[Jekyll Structure](https://jekyllrb.com/docs/structure/)  
[jekyll-theme-chirpy Wiki](https://github.com/cotes2020/jekyll-theme-chirpy/wiki)  

## GitHub Pages & Jekyll
If you don't know, GitHub Pages is a service provide for free to host static website built with Jekyll.  
Jekyll on the other hand is a static website generator, it has the ability to cover markdown files to HTML. On top of that, Jekyll also have a ton of themes to choose from.  
This makes adding content dramatically easy with the help of git.

## Install Jekyll
To ensure everything works like intended, I strongly recommend install Jekyll and test the site on your local machine before pushing.  
Please follow [Jekyll Install Guide](https://jekyllrb.com/docs/installation/) and install it on your local machine. The guide cover how to install Ruby, Bundle and Jekyll, also covered how to add Jekyll to your system's environment variables.  
Make sure you have `git` installed too, `git` is required to clone the repo and push updates.  
[How to install Git](https://git-scm.com/downloads)

## Test Locally
After installing Jekyll, let's make a fork of our website.  
![how2forkstep1](/assets/img/2024-05-29-how-to-contribute/screenshot2024-05-29-17-05-42.webp){: w="600" }
This will make a whole copy of our website and forked it under your user.  
Now just clone the repo you on to your local machine.
```bash
git clone https://github.com/<your-github-username>/itslc2023.github.io
```
Let's go into that directory and run:
```bash
# Install all dependencies for the website and theme
bundle install
# Run the website on your local machine
jekyll server
# The command below will make sure that you are running the right version of Jekyll
# https://jekyllrb.com/tutorials/using-jekyll-with-bundler/#serve-the-site
#bundle exec jekyll server
```
You will see something like this:
```bash
colgrave@lacey:~/Documents/git/itslc2023.github.io$ jekyll server
Configuration file: /home/colgrave/Documents/git/itslc2023.github.io/_config.yml
            Source: /home/colgrave/Documents/git/itslc2023.github.io
       Destination: /home/colgrave/Documents/git/itslc2023.github.io/_site
 Incremental build: disabled. Enable with --incremental
      Generating... 
                    done in 0.644 seconds.
 Auto-regeneration: enabled for '/home/colgrave/Documents/git/itslc2023.github.io'
    Server address: http://127.0.0.1:4000/
  Server running... press ctrl-c to stop.
```
This means that the website is running on `http://localhost:4000`, you are free to make changes and Jekyll will live update the website.  
> Don't forget to refresh the page to see the changes : )

For website's config or layout changes, remember to restart the Jekyll server to see the changes.

## Start Writing
### Structure
Jekyll has a directory structure, see [here](https://jekyllrb.com/docs/structure/). So let's just follow that.  
All post should under `_posts` directory. And please follow the naming scheme: `YYYY-MM-DD-name-of-the-post.md`. 
All images should under `/assets/img/<YYYY-MM-DD-name-of-the-post>/<image.webp>`. I highly recommend using `webp` images, this will speed up page loading time.

### Front Matter
Make sure you have Front Matter on every post. This is mandatory, otherwise the post won't show.
```md
---
layout: post
title: Example Post
date: YYYY-MM-DD 17:12:33 −0500
categories: <categories> <sub-categories>
tags: <tags> # TAG names should always be lowercase
author: <author-id>
image: /assets/img/2024-05-29-how-to-contribute/screenshot2024-05-29-17-05-42.webp
# This is the preview image, details see here: https://chirpy.cotes.page/posts/write-a-new-post/#preview-image
---
Start writing here...
```
[Chirpy Doc front-matter](https://chirpy.cotes.page/posts/write-a-new-post/#front-matter)
### Add Yourself As An Author
This will make your name appear under the title and link it to your website.  
*Optional, but nice to have*   
First you need to add author information in `_data/authors.yml`, and then adding `author` variable to your post's Front Matter like this:
```md
---
author: <author_id>                     # for single entry
# or
authors: [<author1_id>, <author2_id>]   # for multiple entries
---
```
Details see [here](https://chirpy.cotes.page/posts/write-a-new-post/#author-information).

### Markdown
Jekyll is basically a Markdown to HTML converter. All your posts should be Markdown files, `.md` as file extension.  
I'm only going to touch on some of the things we need to pay attention to. If you need help with Markdown please see [here](https://www.markdownguide.org/cheat-sheet/)

#### Heading
Chirpy is weird. After some testing, the heading should always start with `##`, not `#`. Using `#` heading will result content catalogs on the right side not display properly.

#### Links
URLs like: https://jekyllrb.com/ won't have a hyperlink to it, you have to put `[name-of-the-link](https://example.com)` around it.

#### Images
Beside all the image settings Markdown can do, Chirpy Theme also have a lot of image settings.  
Rather of struggling with HTML code, we can just read [here](https://chirpy.cotes.page/posts/text-and-typography/#images).

#### Videos
YouTube videos can also be implemented nicely in to the post like this: `{% include embed/youtube.html id='tpiyEe_CqB4' %}`  
Example:  
{% include embed/youtube.html id='tpiyEe_CqB4' %}

# Pull Request
After pushing the finish product to your own repo, now let's **Merge and ship it!**  
Go back to our site's repo and just click `Create Pull Request`, now just sit back and relax, the maintainer will get notified and happily merge it.  