---
layout: post
title:  "Getting my first post up"
date:   2020-02-13 13:53:29 +0800
categories: jekyll update
---
After spending a couple of months in my to-do list, this blog finally materialized. My motivation behind this is mainly to document my side projects and hopefully it can be helpful to someone out.

Right off the bat, I had some trouble setting up GitHub Pages. I followed the official instructions [here](https://help.github.com/en/github/working-with-github-pages/creating-a-github-pages-site-with-jekyll) but there were a couple of gotchas:

1) Make sure you install the right version of Jekyll that is supported by GitHub Pages
- Check which is the right version from [here](https://pages.github.com/versions/)
- Install it  
e.g. `gem install jekyll -v 3.8.5`

2) When generating the site for the first time, make sure you include underscores around the VERSION like so   `jekyll _3.8.5_ new .`

3) Tip I found from searching repos on GitHub: automatically grab the correct version dependencies in your Gemfile  
```
require 'json'  
require 'open-uri'  
versions = JSON.parse(open('https://pages.github.com/versions.json').read)  
gem "github-pages", versions["github-pages"], group: :jekyll_plugins
```

And all is well again.
