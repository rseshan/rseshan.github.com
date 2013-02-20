---
layout: post
title: "Check Yo <em>Self</em> Before You Wreck Yo <em>Self</em>"
date: 2013-02-20 04:25
comments: true
categories: 
---

<p>Who am I?  Man's age old question is the same one I've been asking myself in Ruby over the last few days.  The key word <em>self</em> is the embodiment of the question, with a slight twist.  In Ruby, everything is an object, and there is one and only one current object at a given point.  This current object is <em>self</em>.  Depending on where you are in the program, <em>self</em> will be different.  Here are some examples to illustrate how <em>self</em> changes depending on the context of the situation.</p>

<h2>Context 1: Top-Level</h2>
<img src="http://rseshan.github.com/images/top_level_self.png">
<p><em>Main</em> is the default top level object that <em>self</em> refers to, and <em>main</em> itself is an instance of an object.  <em>Self</em> in top level methods reference whatever object the method is being called on.

<h2>Context 2: Classes/Modules</h2>
<p>Here, self is the Class or Module object.</p>
<img src="http://rseshan.github.com/images/class_module_self.png">
<p>So, we've seen <em>self</em> go from top-level <em>main</em> to individual Classes and Modules.</p>

<h2> Context 3: Instance and Class Methods</h3>
<img src="http://rseshan.github.com/images/methods_self.png">
<p>The key here is that a method is telling an object what to do, so <em>self</em> within a method is always the object on which the method is being called on (the receiver of the message).  When we first created the instance of the Class Rapper (<em>ice_cube = Rapper.new</em>), and subsequently called <em>time_period</em> on that instance, <em>self</em> is referencing that specific instance, and denotes it by the <em>#Rapper:0x bunch of digits</em>, which is the memory location of that instance.  We see that when we call the <em>consensus</em> method on that instance, we get the same object (<em>self</em>) confirmed by the same reference number.  However, if we look at the class method <em>self.consensus</em>, the object in <em>self</em> is the class Rapper.  Of note, defining the method as <em>self.consensus</em> would have been equivalent to writing <em>Rapper.consensus</em>, which underscores that <em>Rapper = self</em>.  In summary, <em>self</em> can be representing the Class object or an instance of the Class object depending on the context.</p><br>

<p>For further reading, check it yo:<br>
<a href = http://www.jimmycuadra.com/posts/self-in-ruby>Jimmy Cuadra: Self in Ruby</a><br>
<a href = http://sidtalk.wordpress.com/2008/10/06/what-exactly-is-ruby-self/>Sid's Weblog: What Exactly is Ruby Self</a><br>
<a href = http://paulbarry.com/articles/2008/04/17/the-rules-of-ruby-self>Paul Barry: Rules of Ruby Self</a><br>
</p>

<p>And last but not least, here's Ice Cube's words of wisdom on the subject...
<iframe width="560" height="315" src="http://www.youtube.com/embed/CLyS9gz307Y?rel=0" frameborder="0" allowfullscreen></iframe></p>