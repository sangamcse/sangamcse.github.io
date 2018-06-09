---
layout: post
title: "GSoC '18 Post #1: Community bonding ends"
date: 2018-06-07 00:57:20 +0530
description: Community bonding of Google Summer of Code 2018.
img: coala.png
tags: [GSoC, coala, community-bonding]
---

To know about [coala](https://coala.io), go through the
[gsoc-with-coala](http://www.meetsangamcse.me/gsoc-with-coala/) post.

## Project abstract

The aim of the project is to improve linter bears in coala by improving the
testing API that adds support for global bears, adding base test helper class,
automating the tests for bears, adding support for 7 additional linter bears
and enhancing the documentation for coala API and coala-bears.

### Project Mentors:

- [Niklas Meinzer](https://github.com/NiklasMM)
- [Ipshita Chatterjee](https://github.com/IpshitaC)
- [Abdeali Kothari](https://github.com/AbdealiJK)
- [Max Hahn](https://github.com/Mixih)

## What are Linter Bears ?

[`Linter Bears`](http://api.coala.io/en/latest/Developers/Writing_Linter_Bears.html)
word is a combination of the two terminologies: Linter and Bears.
[Linter](https://en.wikipedia.org/wiki/Lint_(software)) is a tool that analyses
source code to flag programming errors, bugs, stylistic errors, and suspicious
constructs. Bears in coala is meant to do some analysis on source code. It can
check your code for potential problems, calculate metrics and even provide
corrections for your code.

[Linter Bears](http://api.coala.io/en/latest/Developers/Writing_Linter_Bears.html)
are bears that are capable of wrapping third party open source linters, and to
be sustainable even allows you to write custom code analysis routines, thus
extending the modular functionality of coala. You don't have to go through the
hassle of learning how to use various tools for different programming
languages. With over 45 supported languages(and counting), things get much
simpler under a single roof.

## Community Bonding Period

The Milestones of my Project during Community Bonding Period are:

- Get in touch with the mentors via [Google Hangouts](https://hangouts.google.com/)
, [Gitter room](https://gitter.im) and
[devlogs](http://www.meetsangamcse.me/project-track/).
- Make a [coala Enhancement Proposal(cEP)](https://github.com/coala/cEPs/pull/149)
of coala's Bears Testing API and get it merged.
- Get assigned to all the issues of the project and finalise tasks to be
implemented in Coding Phase-I.

## Conclusion

On 14<sup>th</sup> May, the community bonding has come to an end and I've
nearly managed to complete my milestone. My earlier contributions to coala
helped me to get knowledge about the [`linter` class](http://api.coala.io/en/latest/coalib.bearlib.abstractions.html#module-coalib.bearlib.abstractions.Linter)
of coala. It has been a wonderful time so far. I've managed to get
[cEP-0027](https://github.com/coala/cEPs/blob/master/cEP-0027.md) merged.

Thats all for community bonding !
Stay tuned ! Till then, Happy Coding !
