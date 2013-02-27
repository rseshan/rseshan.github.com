---
layout: post
title: "Noob Tips: Make Your Ruby Code More Readable"
date: 2013-02-26 06:29
comments: true
categories: 
---

<p>Ruby is an expressive and beautiful programming language.  Ruby code is supposed to be readable enough that if you gave a non-programmer read basic lines, they'd be able to figure out what was happening.  Having readable code will benefit you not only today, but when you might need to look back and try to make heads or tails of the code you wrote months or even years ago.  Just as important, those you collaborate with and others who look at your code won't curse your name under their breath as they read it.  Unfortunately, as a noob, I repeatedly found ways to mangle and uglify my code.  Don't be me.  Here are a few tips to make your code look, read and perform better.</p>

<p><strong>1) Spacing: two (indent), one (commas, colons, semicolons and "{}") and none ("()", "[]").</strong>  Indenting lines with spaces and aligning blocks of code that belong together creates a structure similar to searching through folders and directories.  It makes it easier to follow the logic and for others to read your code.  Don't use the hard <em>tab</em> button UNLESS you've changed the functionality of the <em>tab</em> button to just add 2 spaces automatically.  For instance, <a href="http://www.sublimetext.com/docs/2/indentation.html">Sublime (text editor)</a> allows you to set the "indent" (pressing <em>tab</em>) to actually generate two spaces instead of a hard tab.</p>
<img src="http://rseshan.github.com/images/spacing.png">

<p><strong>2) Comments: less is more.</strong>There is a fine line between overcommenting and undercommenting.  Your code should be expressive enough that you shouldn't need to comment how it works.  If it's not, that's a reason to refactor the actual code rather than comment more.  Get rid of old comments, pseudo-code or old commented-out snippets.  So when to comment?  How to use your code and some code author/creator information are good reasons to comment.  When in doubt, err on the side of brevity.</p>

<p><strong>3) 80 character limit and aligning parameters.</strong>  Long lines are hard to read, and cumbersome if you have to scroll horizontally to read them.  Keep your lines short < 80 characters.  If you have a lengthy parameter/argument list, separate them and align them.  You want your reader to read your code from top-to-bottom, not left-to-right.</p>
<img src="http://rseshan.github.com/images/alignment.png">

<p><strong>4) Naming: variables and methods, Classes and Modules, CONSTANTS.</strong>  Variables and methods should be lowercase, Classes and Modules should be <a href="http://en.wikipedia.org/wiki/CamelCase"><em>CamelCase</em></a> and constants should be all-caps.  Don't use variable or method names on the <a href="http://ruby-doc.org/docs/keywords/1.9/">ruby keywords list</a>.  That's a recipe for disaster and confusion.</p>

<p><strong>5) Be concise and DRY.</strong>  Don't Repeat Yourself is a dictum of the Ruby programming language.  If you see yourself writing the same lines of code over and over, you can probably encapsulate the logic into a single method.  Similarly, don't write in 3 lines of code what you could write in one.  Starting out, my initial goal was to just get my program working.  Then, I would reread the code and refactor to make it more concise and reduce redundancies.  The more code I write and reread, the more patterns I see, allowing me to refactor on the fly rather than waiting till the end.</p>
<img src="http://rseshan.github.com/images/simplify.png">

<p>Use common sense.  You want the code to be consistent, organized, concise and self-explantory.  For more on Ruby style, syntax and conventions, I highly recommend this <a href="https://github.com/bbatsov/ruby-style-guide">Ruby Style guide</a>.</p>