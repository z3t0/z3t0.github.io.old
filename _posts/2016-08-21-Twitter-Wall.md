---
title: Twitter Wall
categories: [projects]
tags: [twitter, node]
---

Recently I have spent some time working on creating a simple twitter wall application using [Electron][1] as the front end, which is a nice framework that allows you to use web technologies to create desktop applications. The application also uses a nodejs [twitter][2] library which implements the official Twitter API which allows it to catch any tweets with specific keywords.

The idea behind this project is to create a very simple twitter wall project, which will eventually be released as an opensource github repository once I have things working nicely.

### Screenshot tracking "olympics" keyword ###

![Screenshot](/images/res/twitterwall-1.png)

### TODO
- Profanity filter
- Retweet specific posts, can act as a bot
- Smooth scrolling and scroll lock aware
- Content support; video and image
- Relative design
- Nicer font

[1]: http://electron.atom.io
[2]: https://www.npmjs.com/package/twitter
