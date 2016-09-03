---
title: Playing With Pixels
date: 2014-09-10 00:00:00 Z
layout: post
---

I learned how to actually write javascript – rather than just hacking other peoples' code – over a weekend in my early 20s (2006-2007ish). My cable had been cut-off for non-payment (again, early 20s) and I had for some reason downloaded a full, offline copy of the javascript docs. What followed was a lot of moving DOM rectangles around the screen and incredible amounts of Math.random() and setTimeout() to make seizure-inducing, flashing animations.

Before my internet was turned back on, all of this had evolved into a really crude swarm implementation. It was basically a PHP file that could take a BMP file. It would convert each pixels into a bunch of 1x1 &lt;span&gt;'s with embedded RGB codes and X/Y coordinates specified as class attributes.

On page load, a bit of javascript would take each span and randomly place it on the screen. It would then slowly move each pixels into place to form the original image. You can view the original <a href='http://descend.org/neil/swarm.html' target='_blank'>here</a>. (warning, nsfw language and CPU-meltingly bad code. Also gratuitous use of #ff00ff.)

DOM libraries and particle animation have come a long way since then. It's now possible (or at least much easier) to load a PNG via javascript and extract all of the pixel information. No server-side parsing necessary.

Belgian agency, <a href='http://digiti.be' target='_blank'>Digiti</a>, the makers of the awesome <a href='http://epicexit.com' target='_blank'>Epic Exit</a> micro-site, released the code that powered Epic Exit as a library called <a href='https://github.com/digiti/MoleculeJs' target='_blank'>MoleculeJS</a>. I decided to take a couple hours to play around with it to see how easy it would be to recreate my old experiment.

It ended up being really, really, stupid easy. And way more performant than the original. First, I drew up a really simple PNG in Illustrator.

![](/images/pixelfuckery/TOODOPE.png)

Then I wrote a bit of inline javascript to create 'molecules' out of the pixels and bend them to my will. The final product was supposed to make it look like the letters are bouncing to some bass, like your blatter the first time you saw the <a href='https://www.youtube.com/watch?v=1koa2xAxCAw' target='_blank'>T-Rex scene from Jurassic Park</a> in theaters.

![](/images/pixelfuckery/toodope.gif)

You can [check out the end result](http://neiltron.github.io/pixeljanks/public/) in your browser and/or [view the code on Github](https://github.com/neiltron/pixeljanks).