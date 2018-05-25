---
layout: post
title:  "Things I Learned Today"
categories: Tech
tags: Jekyll, Markdown
date: 2018-05-23
---

I was working on writing a blog post about libraries and how awesome they can be for people transitioning into the tech world and ended up learning a bunch of little things about Jekyll while I was at it. I still need to proofread and do a bunch of other stuff to the library post, but I want to get something posted this week, so here's some little bits of stuff I learned today.

### Markdown

This isn't actually related to Jekyll specifically, and their [docs](https://jekyllrb.com/docs/home/ "Jekyll Documentation") send you to the Markdown [docs](https://daringfireball.net/projects/markdown/ "Markdown Documentation"). I just want to share them since I'm really enjoying Markdown instead of html for my posts.

Specifically today I utilized: 

1. [links](https://daringfireball.net/projects/markdown/syntax#link "Markdown Links Docs")
2. [lists](https://daringfireball.net/projects/markdown/syntax#list "Markdown List Docs")
3. [headers](https://daringfireball.net/projects/markdown/syntax#header "Markdown Header Docs")
4. [blockquotes](https://daringfireball.net/projects/markdown/syntax#blockquote "Markdown Blockquote Docs")
5. [code blocks](https://daringfireball.net/projects/markdown/syntax#precode "Markdown Code Block Docs")

I love how super simple it is to use and how little it interrupts the reading flow in my .md file. 

### Drafts

Back to Jekyll, I spent awhile trying to figure out how to get drafts to show up when working on development server. In the [Working with drafts](https://jekyllrb.com/docs/drafts/ "Jekyll Working with drafts docs") section it says to create a _drafts folder and put your undated draft post in there. Then run either jekyll serve or jekyll build with the --drafts switch. Seemed simple enough.

Except that my draft post didn't show up when I started the server... The docs say that "Drafts are posts without a date." I checked my frontmatter and it turned out that when I'd copied and pasted the frontmatter from another draft post I'd left the date there. Cool, remove that. Restart server. Still couldn't see my draft posts. 

I poked around a bit more finally found [this article](http://hamishwillee.github.io/2014/06/11/public-drafts-in-jekyll/ "Public Drafts in Jekyll") from 2014 that includes this sentence 

> When you’re ready to publish you simply move the file to the _posts folder and rename it to include the current date.

Ah! I'd gone ahead and put the date I wanted the draft published in the file name. I renamed the file and it worked! Excellent. Turns out that when the docs say "Drafts are posts without a date" they mean "in the file name" not "in the front matter." So I added the date back to the front matter, and it still works.

I wish the Jekyll docs made this a bit more explicit. They do show a folder structure example without the date on the file, but that didn't make it clear to me that the date COULDN'T be included, just that they had chosen not to in this example. 

### Categories & Tags

I'm not currently displaying categories or tags on the blog posts themselves, nor am I listing all the posts with a certain category or tag anywhere. But I am categorizing and tagging all my posts so that I can do that in the future.

Adding categories and tags to posts is a great way of organizing them on your site so others can find information easily. Right now I have two categories "Tech" and "Personal". As well as a few tags. 

Adding them to your post means adding them to the front matter on each post. Jekyll has both category/categories and tags as predefined variables. The front matter for this post looks something like this: 

    ---
    layout: post
    title:  "Things I Learned Today"
    categories: Tech
    tags: Jekyll, Markdown
    ---

There were lots of other tiny things I learned today that I didn't write down and have forgotten about by now but these were the big ones and by far the most useful. 