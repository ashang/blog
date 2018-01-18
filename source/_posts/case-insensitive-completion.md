---
layout: post
title: case insensitive tab-completion or glob expansion
date: 2012-09-09 10:15:00.000000000 +08:00
type: post
published: true
status: publish
categories:
- shell
tags:
- cli
- shell
- bash
---

To let wildcard expansion case insensitive, enable this in `bashrc`:

    shopt -s nocaseglob

To let tab-completion case insensitive, bind `completion-ignore-case` for bash:

    bind `echo set completion-ignore-case on`

This will be effective immediately.

Or add this in `inputrc` for readline:

    set completion-ignore-case On

Include the system inputrc file:

    include /etc/inputrc

To show all binds:

    bind -p

To let bash recognizes spelling mistakes, add in ~/.bashrc:

    shopt -s cdspell

For tcsh / zsh users:

    set complete enhance

Reference:
- http://www.caliban.org/bash/index.shtml#completion
- https://wiki.ubuntu.com/Spec/EnhancedBash
