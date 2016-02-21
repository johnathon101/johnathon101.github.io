---
layout: post
title:  ".Net Core on Linux"
date:   2016-02-20 21:39:09
categories: coding featured
---

I have a great appreciation for Visual Studio as an IDE for the .NET framework. It has a lot of features that make serious development significantly quicker and with less research time for methods within the codebase. That being said there are days where working with a lightweight editor and working in the command line sounds phenomenal. I have been following the .Net core project and recently was able to try the release candidate. It took a couple of hours and I was able to get a working MVC application running on AWS using the Roslyn compiler and hosted using Kestrel. 

There are some great guides online to get it up and running, including this one from Microsoft. <a href="http://docs.asp.net/en/latest/client-side/yeoman.html.">MS Yeoman Guide</a> The scaffolder uses node to generate the .Net framework you are targetting. Once it is created, whichever editor you favor can be used to build out the codebase, but VSCode is handy because it has some idea of the dependencies of the project. Everything else can be ran from the comand line using the .Net cli. Simple commands like dnu restore(updates packages), dnx build(outputs built project to bin folder), and dnx web(deploys development server) make working in the development environment a breeze.
Once the project is built, it is as simple as setting up an instance on AWS using Apache and running the Kestrel server from behind a proxy. I used nginx because it is what I am most familiar with. Overall I was suprised with how few hiccups I ran into being that it is in release candidate status. I had originally built my test site on the beta version and updating it to rc1 was a breeze.

It is exciting to see what new combinations this opens for the .Net community. With Postgres as the go-to data layer for Linux machines in web development, the cost to develop should decrease siginificantly for those who move off the usual IIS/SQL Server combinations. The jury is still out on performance and reliability because the software does not have a complete version but I feel I am one step closer to being able to develop complete .Net solutions in a machine agnostic environment.
