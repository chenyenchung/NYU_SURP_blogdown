---
title: Naming files
date: '2022-06-14'
slug: naming-files
categories:
  - Tips
tags: []
subtitle: ''
summary: ''
authors: ['ycc']
lastmod: '2022-06-14T11:16:10-04:00'
featured: no
image:
  caption: ''
  focal_point: ''
  preview_only: no
projects: []
draft: true
---

> There are only two hard things in computer science: cache invalidation 
> and naming things.
> -- [Phil Karlton](https://www.karlton.org/2017/12/naming-things-hard/)


When start working with R or other languages, [setting a path](https://nyusurp.github.io/2022/06/14/working-directories/) 
is often difficult enough.

To make things more complicated, there are some file and directory names that 
could make things even trickier:

### Special characters and spaces

They often mean something special for your computer:

- `*` and `?` are often used as wildcards to match any character
- `()` and `[]` are used in regular expression to specify patterns
- `<` and `>` are used in *nix systems to redirect the output of a command
- `|` passes the output of a command to another command in *nix systems
- Spaces are often used to separate commands and their arguments

As a result, using those to name your files and directories is likely to result 
in a path that needs to special care and should be avoided if possible. If you 
must use special characters in your file and directory names, there are usually 
ways to tell the computer / programming languages to ignore their special roles.

This is often called _escaping_ and done by put a backslash before the special 
character in many programming languages.

### Non-ASCII characters
