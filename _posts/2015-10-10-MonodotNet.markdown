---
layout: post
title:  ".Net Development in Mac OSX"
date:   2015-10-10 22:10:09
categories: coding featured
---

Visual Studio is a tremendous tool for quickly generating sound projects in Asp.Net. It is developed on the Windows operating, for the operating system. As a developer who quickly grew fond of an OS based on linux, and great hardware, it has been a desire of mine to develop natively without running VMs. This was put on the back burner because the need had not been present. I was invited to talk about Asp.Net development with some students, and asked if the code base could be run on a Mac. It was a fun night to try to get my favorite toolset running in a Mac dev environment. Here are the tools I used:<br>
	* Xamarin Studio
	* Mono Framework
	* PostgreSql
This setup is, by nature, unorthodox in the .Net world. It has some flaws, there are issues to overcome that would never arise by developing in Windows. That being said, overcoming those challenges helps to make me a better developer because the solutions are low-level. The packages used are as follows: Entity Framework 6.1.3, AspNet.Mvc, Razor, WebPages, Infrastructure, Npgsql, Npgsql.EntityFramework. The last two packages allow Postgres and Entity Framework to communicate with as few hiccups as possible.

Once you have the packages installed you must setup your context and database connection to begin communicating with the database.

As long as the names of the columns in postgres match your model properties, they will be automatically tracked by the Entity Framework. Else, a tool like Automapper can be used with a POCO to avoid manually assigning each database property to a model property. The full source for this project is <a href="https://github.com/johnathon101/ToDoAspNet">here.</a>
