---
title = Introduction to Emacs
speaker = Tushar Tyagi
meetupEventId = 235036208
meetupMemberId = 83772362
tags = "Emacs"
---

Emacs is one of the oldest text editors in use today and for good reasons. It is extensible in every way possible with thousands of plugins, supports a lot of programming languages,  is very light on system resources, but unfortunately has a steepish learning curve. In this presentation we will see what it is, and will have a quick tour of its features and some popular plugins.

* Emacs

A case for the awesomeness of emacs.

* What is Emacs?
  - Extensible, Self Documented text editor
  - Not an IDE per se, but can behave like one
  - Also, it is a fully fledged lisp interpreter.
  - Portable. Core in C, the command interpreter in a Lisp dialect

* Why to use it?

** Because of the design philosophies
   - Efficient workflow since there's almost no context switching
   - Hands only use keys, not mouse.
   - Everything is text -- including network calls, shells, applications.
   - Manipulate the text using keys.
     * Keybindings can be changed
     * And get ingrained in muscle memory
     * But also follow a general pattern

** Extensibility
    - Has always been extensible
      + Before WWW the extensions were available on private ftps
      + Currently we have package repositories
    - Bend it to your will
    - It is a programming language which can do anything

** Others
  - Joke: Is it an amazing OS without a decent editor?
  - It has (almost) everything you could think of doing.
  - Extremely light on resources.

* How to use it?

** Vanilla Emacs:
   This is the factory version of emacs with almost no visible bells and whistles, and looks friendly to the people coming from different backgrounds and who are used to using mouse.
   This gets boring quickly since emacs is all about customization.

** Spacemacs:
   A pre-customised version of emacs with support of a lot of languages out of the box. Other things can be added as required.

** Preludes:
   Some of the experienced emacs users have shared their configuration online which can be cloned and used as a base.

** Custom Build:
   Hack together the bits and pieces of the editor.
   Learn ELisp in the process and extend the editor.
   Use packages to extend.

* A little Introduction: Terminology

** Frame
   What we call a "window" generally is called a frame in emacs. Right now I have one frame. There can be more than one frame, which makes a lot of sense in the multi-monitor setup. These frames can connect to one another and share all the contents.

** Buffer
   What is being shown on the screen. This is an abstraction of "something" which can be a file, a process, etc.

** Window
   This is what is being shown to the end-user and contains exactly one buffer. The buffers can be swapped in and out of windows and there can be more than one window in any given frame.

* A little Introduction: Modes
  - Modes add interactivity and life to the otherwise dead text files.

  - Modes are written in emacs lisp, and change the behavior of the text on the fly.  

  - 2 types, Minor and Major. Major modes are functionality, minor modes are enhancements.

  - Each buffer can have one major mode and any number of minor modes active at a given time.

* Minor Mode: Helm
  Looks for patterns in the buffers, commands, documentation, and in almost everything that is there in emacs.

  Swoop, `locate`, `man`, whoa!

* Minor Mode: Projectile
  Used for project management and allows easy jump between projects. Add to that the power of helm and it knows more about your project than you do!

  It allows for searching files, searching inside files, dired the project, run version control, run shell, etc.

* Minor Mode: Paredit
  Very, very useful for Lisp based languages: CL, Scheme, Clojure, etc.

  This matches the number of opening and closing parenthesis so that you don't have to, and allows you to work directly with S-expressions.

* Minor Mode: YASnippets
  Save typing and use snippets.

  YAsnippet uses a mini language which you can use to create new snippets.

  Snippets can include lisp to use the power of emacs.

* Minor Mode: Multiple Cursors
  Everyone knows about this. Emacs has this via a package.

* Minor Mode: Magit
  One of the best integrations/package in emacs. It is a full fledged git client working in emacs.


* Minor Mode: Gist
  Gist-mode allows integration with Github's Gist. You can create gists from the buffers, push them, fork them, delete them, and do everything that is possible on the Gist website.

* A little Introduction: Major Modes
  At least in programming context, major modes are specific to a given language or technology.

  The functionality varies and ranges from basic text-highlighting to debugging and refactoring. Others manipulate the text in previously unthinkable ways.

  We will look at implementing factorial in different languages.

* Major Mode: Python Mode
  The package `elpy` provides a great python experience with syntax checking,  PEP-8 recommendations, unit testing, etc.

* Major Mode: Lisp/Scheme Mode
  SLIME provides a great REPL for Common Lisp.

  For Scheme/Racket, we have Racket-Mode which supports both scheme and racket REPL.

* Major Mode: JS Mode
  JS2-Mode provides the functionality for Javascript REPL using a node backend. There is also support for syntax highlighting and intellsense using tern.

* Major Mode: Latex Mode
  Want to write a lot of scientific formula? Emacs supports Latex support out of the box using Auctex plugin.

* Major Mode: Elfeed
  Allows you to read RSS feeds without leaving the comfort of emacs. The feeds can be tagged, marked, saved, and of course, you can copy the quotes out of these.

* Major Mode: Org Mode
  Now for something completely different...

  Org mode is a world in itself and showcases what can be done using just text. It can transform plain text to provide:

  - Todo lists
  - Agendas
  - Schedule timelines to lists and agendas
  - Literate Programming
  - Support for exporting into a lot of formats (Markdown, Pdf, Html, etc.)
  - And much, much more.

* A Digression into macros

  These are nothing like C macros.

  Sometimes a lot of editing is repetitive across lines, entire text or files.

  Emacs provides the functionality of storing your repetitive keypresses and repeat these to edit text.
