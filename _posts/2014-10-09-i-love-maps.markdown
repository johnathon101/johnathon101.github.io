---
layout: post
title:  "I Love Google Maps"
date:   2014-10-09 22:10:09
categories: rubyonrails featured
---

I have a few rails projects living in the wild now and the majority of them use the google developer
api. It amazes me how much information I can wrangle for free and split it up to do my bidding. In
Rails, I am using the gon gem to get lat/lon coordinates over to the javascript to make markers on
my maps. The gon gem creates your rails variables in json and you can use it in your javascript, it's
pretty awesome. However, like anything automagic, there are multiple ways to do things and sometimes
I can't tell which is best. The gon gem has been bulletproof regarding reliability and is a cinch to
setup. However, while I was debugging some code with a developer, I saw they had made a controller
action, route and an ajax call from the javascript to the controller to get the
data. It was a moment of realization that my tried and true method of using a gem may be the lazy
one. Then again, in the time it would take me to build the route, controller, rescue and ajax call
it would take five times as long and arguably be nearly the same outcome as using gon.

<br>
Outside of moving data, the google developer api is just great to work with. The documentation is
outstanding. On my current project I am moving data to the javascript in one action, and letting
the user modify the javascript object, extracting the changes using an ajax call to a controller
action and storing it in the database. It is a fun circle and I have probably spent as much time
toying with it as creating it. I am currently having fun with oauth and outsourcing my authentication,
if the user desires, to g+, gh, fb and twitter. When I first started making web apps I didn't like sites
that linked other accounts to create your profile. Now I have come to appreciate it. It is a joy to
have so much data, communication control and collaborative potential at my fingertips.
