---
layout: post
title:  "No passwd git pull"
date:   2017-06-27 16:31:13
categories: git
permalink: /archivers/hello
---

## Generate .gitconfig file ##
run the following commond in your repository:

> git config --global credential.helper store

>[credential]

>    helper = store

will be added to ~/.gitconfig automaticly

## Generate .git-credential ##
run: 
> git push 

input your user name and passwd

> https:{username}:{password}@github.com 

will be added into ~/.git-credential automaticly

## Next time passwd is not needed when doing git push ##
**Done!**
