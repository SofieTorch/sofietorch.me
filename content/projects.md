+++
title = "Projects"
menu = "main"
+++

Here you'll find projects I'm proud of, each one with a different peculiarity 💜.

<h2 style="margin: 0;">
<a href="https://pub.dev/packages/epub_decoder">epub_decoder</a>
</h2>
<b>Flutter package to parse EPUB files (ebooks), with support for Media Overlays! 🔉📑</b>
<a href="https://codecov.io/gh/SofieTorch/epub_decoder" style="text-decoration: none;"> 
 <img src="https://codecov.io/gh/SofieTorch/epub_decoder/graph/badge.svg?token=0D5LI5EWM6"/>
</a>
<img alt="Pub Points" src="https://img.shields.io/pub/points/epub_decoder">
<a href="https://pub.dev/packages/epub_decoder" style="text-decoration: none;">
  <img alt="Pub Version" src="https://img.shields.io/pub/v/epub_decoder?color=blue">
</a>

While I was looking for ebook readers to use, I saw that some of them have a “read aloud” feature, which is the synchronization between sound and text to highlight the text that is being read aloud.

I became curious about how this synchronization worked and, without realizing it, I ended up reading the SMIL (Synchronized Multimedia Integration Language, more commonly known as Media Overlay) and EPUB specifications, which is what is behind this synchronized reading (plus [this amazing](https://www.oreilly.com/library/view/epub-3-best/9781449329129/ch01.html) book).

But these specifications only define how to structure the files so that they can be synchronized, the synchronization itself is something we have to do for ourselves.

So I started looking for how this is implemented in open source projects that read EPUBs in Flutter, and to my surprise, I didn't find any that included reading media overlays (and thus synchronization). So I decided to implement it myself 💙.

Discover its functionalities and how to use it in your Flutter project **[on pub.dev](https://pub.dev/packages/epub_decoder)**, and don't forget to **[leave a star on GitHub](https://github.com/SofieTorch/epub_decoder)** if you find it interesting! ⭐

---

<h2 style="margin: 0;">
<a href="https://github.com/marketplace/actions/find-and-lowercase">find-and-lowercase</a>
</h2>
<b>GitHub Action to find regex matches on files and transform them to lowercase 🔍🔡</b>
<img alt="GitHub Tag" src="https://img.shields.io/github/v/tag/sofietorch/find-and-lowercase?label=version&color=green">

During my time working at University of Valley, I had to create documentation about the redesign of the mobile app, and for this I used [DartDoc](https://pub.dev/packages/dartdoc) (for API docs) and [Retype](https://retype.com/) (for Markdown docs).

However, when generating the documentation website, all the links to the API docs were broken, and I discovered that it was because of the Retype build, which renamed all the files to lower-case. **[Here you can see the issue I opened about it](https://github.com/retypeapp/retype/issues/302)**.

Luckily the Retype team was able to solve the bug in a few weeks, but as I needed to generate the docs site quickly, I created [this GitHub Action](https://github.com/SofieTorch/find-and-lowercase), which according to a regex pattern, converts all matches inside the files of a directory to lower-case. This way the links inside the docs would point to the files with their new lower-case name (after the Retype build) and no links would be broken.

It was a small but very useful project, plus it was the first time I created a GitHub Action **[and published it](https://github.com/marketplace/actions/find-and-lowercase)** in case, for some reason, someone else needs it to save themselves in a hurry.

---

<h2 style="margin: 0;">
<a href="https://github.com/SofieTorch/pictify">pictify</a>
</h2>
<b>Flutter plugin for image processing using C++ capabilities 🖼⚡</b>

During college I took the Digital Image Processing course, where I learned different methods and algorithms in C# to, redundantly, process images.

But something that bothered me was the speed issue, since it took a few seconds or even a minute or two to perform certain types of processes. First I replicated these processes on my own with Python and Numpy, as it is used quite a lot in this area, but because of the interpretation process it takes I didn't think it was the most efficient option at that time (but later I found it can be fast 😅).

That's how I decided to make an **implementation in C++** ⚡, and run it in **Flutter through DartFFI**. I built a package for iOS and Android and it was a success ✔, since the processing was **so fast** that I could even **do it in real time** with a slider (instead of a button and wait, like in college).

However, I didn't publish the package because there are already other good packages like [image](https://pub.dev/packages/image), which still do image processing for Flutter quite well (not in C++, but quite well).

Maybe if the project gets some stars on **[GitHub](https://github.com/SofieTorch/pictify)**, I'll think about publishing it :)
