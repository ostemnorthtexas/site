# oSTEM@North Texas Website

This website uses the [Beautiful Jekyll](https://github.com/daattali/beautiful-jekyll) Theme
(*Copyright 2020 [Dean Attali](https://deanattali.com)*).

This theme's [hard mode install](https://beautifuljekyll.com/getstarted/#install-steps-hard).

## How Jekyll Works

Jekyll is meant for blogs, but it makes beautiful websites.
With the exception of the index.html page, all of these are formatted in
Markdown.

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

Adding the below code to a MD file generates a table of contents of the page.
```
* TOC
{:toc}
```

## Web Accessibility

Before releasing this website into the unknown, **PLEASE** make sure it has
passed an accessibility check.
If it is failing on contrast checks in the title, that's tolerable based on
how this template is set-up. Make it as readable as possible.
But things like alt text and Aria labels are mandatory.
Also, please consider whether any linked content is appropriated captioned.
- [WebAim Contrast Checker](https://webaim.org/resources/contrastchecker/)
- [WAVE Web Accessibility Evaluation Tool](https://wave.webaim.org/)
- [WAVE Browser Extension (works on `jekyll` test site)](https://wave.webaim.org/extension/)
- [Color Oracle - Color Blindness Simulator](https://colororacle.org/)
