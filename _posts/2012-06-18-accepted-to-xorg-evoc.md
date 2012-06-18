---
layout: post
title: "Accepted to X.Org EVoC"
category: "Piglit"
tags: ["EVoC", "Piglit"]
---
{% include JB/setup %}

A few weeks ago I sent a project proposal to [X.Org][1]'s [Endless Vacation of Code] [2] (EVoC).
It was about adding OpenCL testing framework to [Piglit] [3] - the testing suite for OpenGL implementations.
On 7 June 2012 I was thrilled to hear that my project was accepted and I've started working on it immediately in the following week.

As you've probably calculated I'm a little bit late with my first post, but I will try to deliver new posts on time.
With this and [following] [5] posts I am planning to document all the work that will go into this project.

_For those that don't know what X.Org EVoC and Piglit are:_

+ [_X.Org EVoC_] [2]:
  _EVoC stands for Endless Vacation of Code. It's basically a [Google Summer of Code] [6] clone, that is targeted at X.Org's projects and sponsored by educational non-profit X.Org organisation.
   It was created because Google couldn't accept all the students with good project proposals and it was only active in summer time.  
   The projects on X.Org are mostly connected to open-source graphics. If you are a student and want to contribute to this community check other [project ideas] [7]._

+ [_Piglit_] [3]:
  _Piglit is a testing suite for OpenGL implementations targeted at developers.
   It is used to test OpenGL and OpenGL ES state tracker and driver conformance.
   It is mostly used in open-source Linux drivers._

## Project details

In 12-16 weeks I plan to implement framework for writing OpenCL tests and of course write a lot of tests. The plan that I am trying to stick to is as follows:

+ __Week 1__: Study Piglit’s design. Start implementing utilities to support OpenCL testing.
+ __Week 2__: Continue implementing utilities for the framework. Implement tests for context independent API functions.
+ __Week 3-4__: Add support for choosing platform and devices. Implement API tests for manipulating context, memory objects and queues.
  Implement tests for API functions that depend on kernels (with simple or empty kernel).
  Extend framework as needed.
+ __Week 5__: Extend framework to compile and execute an arbitrary kernel.
+ __Week 6__: Write a lot of kernels to test compiler conformance.
+ __Week 7__: Extend framework to support predefined inputs and outputs for kernels.
  Add support for defining how kernels are executed (data-parallel/task-parallel, number of dimensions, work-group size).
+ __Week 8-9__: Write a lot of kernel tests to test for all kinds of possible errors.
+ __Week 10-11__: Write more kernel and API tests, fix simple bugs in CLover and Gallium3D drivers, report complex bugs.
  Integrate tests into Piglit’s HTML result viewer.
+ __Week 12__: Clear up all the code, improve code readability, improve documentation.

I am currently in my second week of development and I still have to post about my work over the first week, so expect a new post with more Piglit details soon...

[1]: http://www.x.org/wiki/Home "X.Org homepage"
[2]: http://xorg.freedesktop.org/wiki/XorgEVoC "X.Org EVoC webpage"
[3]: http://piglit.freedesktop.org/ "Piglit homepage"
[5]: {{ site.JB.categories_path }}#Piglit-ref "{{ Piglit }} posts list"
[6]: https://code.google.com/soc/ "GSoC homepage"
[7]: http://www.x.org/wiki/SummerOfCodeIdeas "EVoC project ideas"
