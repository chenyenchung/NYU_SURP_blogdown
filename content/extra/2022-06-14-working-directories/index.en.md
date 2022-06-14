---
title: "Working directories"
authors: 
  - 'ycc'
date: '2022-06-14'
slug: working-directories
categories:
  - Jargon
tags: []
subtitle: ''
summary: ''
lastmod: '2022-06-14T00:56:49-04:00'
featured: no
image:
  caption: ''
  focal_point: ''
  preview_only: no
projects: []
---

There are two different ways to represent where a file is: Absolute or relative.

Absolute path for a file is using the root as the starting point (`/` for Linux 
and Mac and `C:\` for Windows). This is usually clear to the computer, but it 
can be really long and not comprehensible to human and thus impossible to wrap 
our heads around it and write.

For example, I had a note stored in `/Users/ycc/Library/Mobile Documents/iCloud~md~obsidian/Documents/YCC/Reading note/@gold.brand_2014.md`. There is no way I can remember this and type it when 
writing a script.

Relative path is much shorter, but it could be tricky because sometimes where 
the path is defined _relative_ to is unclear.

In R, you can find the working directory with `getwd()`, which gives you the 
absolute path of the reference.

Say your working directory is `/Users/me/my_cool_project`, and you have a csv 
file (named `myawesome.csv`) stored in a subdirectory called "data", you can 
write `data/myawesome.csv` in R, and R will append `/Users/me/my_cool_project` 
before your relative path for you.

If you need to ask R to find `/Users/me/a_file_outside_wd.txt` for you, 
relative path still has you covered outside your working directory: `..` means 
go up to the parent folder in relative paths, so 
`/Users/me/a_file_outside_wd.txt` is `../a_file_outside_wd.txt` if your working 
directory is `/Users/me/my_cool_project`.

For tips to set working directories in RStudio, you might also want to check 
[the official documentation](https://support.rstudio.com/hc/en-us/articles/200711843-Working-Directories-and-Workspaces-in-the-RStudio-IDE).
