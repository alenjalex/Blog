---
title:  "Moving from Wordpress to GitHub Pages"
 date:   2018-06-27 14:28:00 +0530
categories: blogging
description: Tuples in C# 7
tag: 
  - jekyll
  - github-pages
  - static-site
---

I have been hosting my blog using wordpress for the past 1 year. Wordpress, although is easy to use, is quite heavy and was too much work for me.

I wanted to write my posts as `markdown` files (which wordpress supports through plugins like [WP Editor.md](https://wordpress.org/plugins/wp-editormd/)).  
But then I wanted to be able to maintain a copy of my markdown files on github. I started a repository on github and pushed markdown files to the repo. Then, I would use the plugin [Mytory Markdown](https://wordpress.org/plugins/mytory-markdown/), which would accept a url to a markdown file and convert that to html and publish. This was a good solution to me, except it was too much work for me.  
I wanted to be able to make changes to a post, or write a new post and just push it to GitHub, which will _magically_ update the blog ... _Somehow_.

That's when I heard about Static Site Generators on the podcase [msdevshow](https://msdevshow.com/). Jason Young of the show has done exactly the same for his blog, which he has written about it [here](http://ytechie.com/2017/11/moving-my-static-blog-to-docker/).

I did my own research and decided to use [Jekyll](https://jekyllrb.com/) which powers [GitHub Pages](https://pages.github.com/). To be able to use Jekyll, we would have to actually host the site on a server or even better on a Storage Service like the [Amazon S3](https://aws.amazon.com/s3/) or [Azure Storage Service](https://azure.microsoft.com/en-us/services/storage/). The idea was to run a function every time a commit was made on the `master branch` of the GitHub repo, run a function which would generate the Static Blog and publish it. Jekyll does a good work at documenting it. You can find it [here](https://jekyllrb.com/docs/home/).

My switch to GitHub Pages
-------------------------

It was during my research that I realized that I could just use GitHub Pages and not worry about hosting at all. I just need to push my post to my GitHub repo and the static site generation and hosting part of it will be taken care by GitHub alone.  
This came as a big relief, now that I don't have to worry about anything but my blog post.