---
layout: post
title:   "When Google Search fails, and when it doesn't"
date:   2014-09-28
categories: articles
tags: [data science, google search, search engine]
comments: true
share: true
---

### What Google can't do

Google (Search) is pretty awesome.  Sometimes it knows what I want more than I know what I want.  But not with punctuation, special characters, symbols, whatever you want to call them -- stuff like `!#$%&*+-/.,;:`

### When I want to search for special characters

I find myself trying to search for special characters in two common situations:

1. **Code:** I'm often googling syntax for whichever programming language I'm coding in.  Code is generally littered with special characters... especially if you're doing something with [regular expressions](http://en.wikipedia.org/wiki/Regular_expression)... like `([[^:]]+)://([[^:/]]+)(:([[0-9]]+))`

2. **Writing:** When I'm writing, I often use Google to help get a feel for how conventional/correct/mainstream the phrase or grammar I'm using is.  If the [New York Times](http://www.nytimes.com/) (or any organization of prestige) uses the piece of language I'm inquiring about, then I feel good about it.  If Google returns only a couple sketchy websites with visibile editing lapses, I'll probably rephrase my language.  Take "editing lapses" for example.  I thought of the phrase just as I was writing the previous sentence you just read.  Having not used the phrase (that I can remember) before, I Googled it.  Sure enough, one of the first hits was the [New York Times Manual of Style and Usage](http://books.google.com/books?id=CnwIVkAQgFwC&pg=PA85&lpg=PA85&dq=%22editing+lapse%22&source=bl&ots=xmq938KI5G&sig=6EAvhXLUvJ0hN7ERVdHvuA6kKg4&hl=en&sa=X&ei=0MwkVM_kINiiyAS7_oD4Cw&ved=0CD8Q6AEwBg#v=onepage&q=%22editing%20lapse%22&f=false):

> If the justification is lame or lacking, the correction should acknowledge reporting or **editing lapses**.

### What special characters Google can do

Google claims to provide search support for [some special characters](https://support.google.com/websearch/answer/2466433):  

* `+`
* `@`
* `&`
* `%`
* `$`
* `-`
* `_`

This wasn't always the case -- checkout [Google's official Search blog post from March 2012](http://insidesearch.blogspot.com/2012/04/search-quality-highlights-50-changes.html).  Search may support these special characters, but it does not allow (from what I can tell) to search for a specific quoted string with the character.  I had decent luck with `$` and `%`, but could barely get any queries to work with `-` or `+`.  

However noticably absent are the comma, period and colon and semicolon which account for nearly all the grammar queries I'd want to run by Google.

It appears I'm not alone.  [Here on Google's product forms page](https://productforums.google.com/forum/#!topic/websearch/JJZ35b1ShFg), a user complains of the same issue -- inability to include a comma in a quoted string query.

### What else Google can do

Google provides the simplicity of one search line that knows all (most of the time).  There's also the [Google Advanced Search](https://www.google.com/advanced_search) page, which is not obviously located on [the main search page](http://google.com), where you can narrow your search by explicity guiding Google.

You can also utilize the simple search bar with basic [Google Search operators](https://support.google.com/websearch/answer/136861?hl=en).  For some reason Google doesn't document all of the operators -- [here is a more extensive list](http://www.googleguide.com/advanced_operators_reference.html).

Some of my favorites are:

* `filetype:pdf` returns just pdf documents... can replace with `:pdf` with `:R` if you're looking for R scripts. You get the idea.

* `"this exact phrase"` returns hits with the exact phrase in quotes

* `d3 -diablo` returns hits on `d3` without the word `diablo`.  This was a problem for me when I was constantly searching for the JavaScript library [D3.js](http://d3js.org/) and not [Diablo 3](http://us.battle.net/d3/en/) which admittedly consumed large part of my life for a short but intense period.

* `link:http://en.wikipedia.org/wiki/Catch-22` returns all the websites that link to the [Catch 22 wiki page](http://en.wikipedia.org/wiki/Catch-22).  I like to use this on new websites/blogs/online-storefronts to scan for any red flags and general clout on the web.

* `~inexpensive dinner` returns hits for inexpensive dinners, cheap dinners, budget dinners, and any synonym of `inexpensive` with dinner.  I've had mixed success with this one.  A lot of the time the results appear the same with or without the tilda `~`.

### Where you can search for special characters

For code specific queries, the Stack Overflow community seems to favor [SymbolHound](http://symbolhound.com/).  For the few queries I tested with special characters, it returned some honest results with my exact string of special characters, but only a few hits (sometimes 2, sometimes 0).

Slightly unrelated... but when you find a special character that you can't identify in a paper, or want to copy that special character somewhere, you can search for it on [amp-what.com](http://www.amp-what.com/unicode/search/)

It's not just Google.  The other big search engines, like [Bing](http://bing.com) don't support the full gamut of special characters either.  I did encounter a new search engine called [Blekko](http://blekko.com) with an interesting service -- [webgrep](https://blekko.com/webgrep) -- that does exactly what I'm looking for.  They search for specific strings of text including punctuation in the raw HTML and rank the top URLs.  The only problem is that it takes 10 hours and is on reqest only.  `:(`  Cool concept though.





