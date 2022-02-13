---
title: "Installing epdfinfo Server Prerequisites on a Debian-based system"
author: ["Vedang Manerikar"]
draft: false
---

First make sure a suitable build-system is installed. We need at least a C/C++ compiler (both `gcc` and `g++`), `make`, `automake` and `autoconf`.

Next we need to install a few libraries `pdf-tools` depends on, some of which are probably already on your system.

```sh
$ sudo apt install libpng-dev zlib1g-dev libpoppler-glib-dev libpoppler-private-dev
```

On some older Ubuntu systems, the final command will possibly give an error. This should be no problem, since in some versions this package was contained in the main package `libpoppler-dev`. Also note, that `zlib1g-dev` was for a long time called `libz-dev`, which it still may be on your system.

Debian wheezy comes with `libpoppler` version `0.18`, which is pretty old. The minimally required version is `0.16`, but some features of `pdf-tools` depend on a more recent version of this library. See the following table for what they are and what version they require.

| You want to ...                           | Required version |
|-------------------------------------------|------------------|
| ... create and modify text annotations.   | &ge; 0.19.4      |
| ... search case-sensitive.                | &ge; 0.22        |
| ... create and modify markup annotations. | &ge; 0.26        |

In case you decide to install `libpoppler` from source, make sure to run its configure script with the `--enable-xpdf-headers` option.

Finally there is one feature (following links of a PDF document by plain keystrokes) which requires imagemagick's convert utility. This requirement is optional and you may install it like so:

```sh
$ sudo apt install imagemagick
```
