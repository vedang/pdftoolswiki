---
title: "About PDF Tools"
author: ["Vedang Manerikar"]
draft: false
---

PDF Tools is, among other things, a replacement of DocView for PDF files. The key difference is that pages are not pre-rendered by e.g. ghostscript and stored in the file-system, but rather created on-demand and stored in memory.

This rendering is performed by a special library named, for whatever reason, `poppler`, running inside a server program. This program is called `epdfinfo` and its job is to successively read requests from Emacs and produce the proper results, i.e. the PNG image of a PDF page.

Actually, displaying PDF files is just one part of `pdf-tools`. Since `poppler` can provide us with all kinds of information about a document and is also able to modify it, there is a lot more we can do with it. [Watch this video for a detailed demo!](http://www.dailymotion.com/video/x2bc1is%5Fpdf-tools-tourdeforce%5Ftech?forcedQuality%3Dhd720)
