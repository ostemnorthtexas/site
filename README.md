# oSTEM@North Texas Website

This website uses the [Beautiful Jekyll](https://github.com/daattali/beautiful-jekyll) Theme
(*Copyright 2020 [Dean Attali](https://deanattali.com)*).

This theme's [hard mode install](https://beautifuljekyll.com/getstarted/#install-steps-hard).

## How Jekyll Works

Jekyll is meant for blogs, but it makes beautiful websites.
With the exception of the index.html page, all of the site pages are formatted
using [Markdown](https://www.markdownguide.org/basic-syntax/).
Because it's hosted on GitHub, it technically uses
[kramdown](https://kramdown.gettalong.org/quickref.html), which is very
similar.
Markdown files can use a mix of HTML and Markdown, so if something is more
easily done in HTML, you can add that raw.

### If You Don't Have Access
Fork this repository on GitHub. Follow the steps for "If You Have Access"
(below) but using your forked copy. When you're ready to update, push the
changes to your fork, and then submit a pull request.

### If You Have Access
To contribute, download the zip files of this folder.
If you're familiar with the command line, you can instead use
`git clone https://github.com/ostemnorthtexas/site.git`.

[Install Jekyll](https://jekyllrb.com/docs/installation/). This can be a process.

Enter the folder you downloaded using the command line.
Run `bundle install` to install the required information.
If Jekyll yells at you, it's probably safe to do what it tells you to do.
You can build a "test site" (local version) to preview the website with
`bundle exec jekyll serve`.
If there are fatal build errors, they will appear in your Terminal.
To exit the local server, use `Cntrl+C` in your connected Terminal.
With the exception of the `_config.yml` file, any updates you make while
"served" should be automatic.

Once you're ready to save what is effectively a checkpoint (as long as it works),
do these three commands.
```
> git add .
> git status
> git commit -m "Info about what I updated"
```
The `"Info about what I updated"` is the commit message, so it should reflect
what you actually did since the last update.

Before trying to submit it to the GitHub repository, run `git pull`.
This will update your local copy with what is online, in case someone else
was making changes at the same time.
If that was clean and there are no messages you have to fix, run `git push`.

## Specific Information

### Front Matter
Each new page begins with what is known as Front Matter.
This is the part that sets up certain variables for the page.
The basic front matter will look something like this:
```
---
layout: page
title: STEM Resources
cover-img: assets/img/headers/milky-way-rainbow.jpg
---
```
The layout is set to `page` (so it's rendered as a webpage, not like a blog
post). The `title` is the page title (both in Heading 1 and in the browser bar),
and the `cover-img` is the image behind Heading 1. The `cover-img` is optional.
The three dashes (`---`) separates the Front Matter from the rest of the page.

### Table of Contents
Adding the below code to a MD file generates a table of contents for the page.
```
* TOC
{:toc}
```

### Images
Images within a page have a specific kind of formatting that references the
HTML. The style they are written in is Liquid (Jekyll really just pulls all
the random formatting things together...).
```liquid
{% include image.html file="../../../assets/img/name-of-file.png"
alt="This is alt text." caption="This is a caption."
max-width="600; I only need this feature if I'm an SVG" %}
```

Any images you add should be in the `assets/img` folder (you can add subfolders
to make it cleaner).

### Font Awesome and Emojis
The (free) Font Awesome 5 stylesheet has been referenced for this site.
You can thus add any free [Font Awesome Icons](https://fontawesome.com/).
An example of one of these icons is the external link for past meetings.
```
<i class="fas fa-external-link-alt" aria-hidden="true"></i>
```
Theoretically, the unicode for Font Awesome should also work.

You can add emoji using their unicode values (with some extra stuff).
For example, a smiley emoji, whose unicode value is U+1F603, would be `&#x1F603;`
in HTML.

### Links
Any external link needs the `http` or `https` designation, otherwise it is
assumed to be a relative link internal to this site.
```
[external link text](https://this-is-my-link-address.com)
[internal link text](/pages/name-of-page)
```

### Highlighted Text
A text highlight can be added using HTML.
```
<span style="background-color: #FFFF00"> Text to be highlighted </span>
```

## Web Accessibility

Before releasing this website into the unknown, **PLEASE** make sure it has
passed an accessibility check.
If it is failing on contrast checks in the title, that's tolerable based on
how this template is set-up. Make it as readable as possible.
But things like alt text and Aria labels are mandatory.
Also, please consider whether any linked content is appropriately captioned.
- [WebAim Contrast Checker](https://webaim.org/resources/contrastchecker/)
- [WAVE Web Accessibility Evaluation Tool](https://wave.webaim.org/)
- [WAVE Browser Extension (works on `jekyll` test site)](https://wave.webaim.org/extension/)
- [Color Oracle - Color Blindness Simulator](https://colororacle.org/)

You can read more about this on the University of Washington's
[Developing Accessible Websites](https://www.washington.edu/accessibility/web/)
page.
