---
layout: post
title:  "Why I Use Vim"
date:   2015-11-11
categories: tools
---

The short answer is that I like it. Vim is almost always available (Unless I
have to use Windows), is incredibly powerful, and I can customize it to look
exactly how I want.

## Backstory

I started out programming with the Visual Basic 6.0, then later Visual Studio
.NET. Starting out with a heavy IDE made some things easier, but eventually I
realized that it is often useful program without the help of code generation,
as the result is often more maintainable.

With html and javascript, I started writing all the code in
[Notepad](https://en.wikipedia.org/wiki/Notepad_(software)). This worked well,
as it was a lot quicker to open than visual studio, and I could use any Windows
computer that way. At work I soon discovered issues with notepad, like it's
complete inability to handle large files. So, I looked around and found
[Notepad2](https://en.wikipedia.org/wiki/Notepad2). I loved it.  Not only did
it have a nice simple interface, it loaded quickly, handled large files, and
included syntax highlighting. I could even run it off of a USB drive, so it was
nearly always available.

Notepad2 was my main editor for a long time, unless I was doing C# apps, in
which case I actually opened up Visual Studio.

A few years later, I discovered emacs. At that point, I was often using linux,
but was far too confused when I accidentally opened vim and couldn't do
anything, not even quit. I discovered that if I changed my EDITOR variable to
emacs, then I could actually figure out waht was going on, and edit files.

I used emacs for several years, and learned the power of using an editor that
can be completely customized. Emacs had it's faults though. For one, it was a
bit slow to load, especially with a lot of plugins. Also, I found myself stuck
using Ctrl and Alt way more than was reasonable, and commands like `Ctrl-x
Ctrl-c` to close a file became a bit annoying at times.

Then about a year or two ago, I saw someone using vim while live coding and I
decided to give it a shot. Initially, I was still a bit lost, but after a few
days I remembered how to switch modes (`i` for insert, `ESC` to get out, `v`
for visual), and how to save and quit (`:wq` in normal mode).

Vim has a brutal learning curve, but after you get comfortable, the power
really shows through. For instance: to reformat the last 3 paragraphs to have a
maximum line length of 80 characters, all I have to do is `v3{ ENTER gw`. The
amazing part though, is that it really isn't terribly hard to remember the
different keystroke combinations, because they all follow similar patterns.
That's not to say it's easy to learn them, but it is easy to build with the
small patterns that you take the time to learn. In the end, it is the
simplicity of the basic components, combined with the composable patterns of
usage that makes Vim as powerful as it is, and that is why I use it.
