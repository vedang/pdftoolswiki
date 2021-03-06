---
title: "Installing pdf-tools"
author: ["Vedang Manerikar"]
draft: false
dirtree:
  display: false
---

Installing this package via NonGNU ELPA or MELPA or any of the other package managers is straightforward and should just work. `pdf-tools` requires a server `epdfinfo` to run against, which it will try to compile and build when it is activated for the first time.

You should not require any manual changes. The documentation below is **only if you are installing from source**, or for troubleshooting / debugging purposes. The following steps need to be followed **in this order**, to install `pdf-tools` and `epdfinfo` correctly:

-   [[8ce3cf4e|Installing `epdfinfo` server prerequisites]]#
-   [[e305cd0a|Installing the `epdfinfo` server]]#
-   [[3d4e6b6b|Installing `pdf-tools` elisp prerequisites]]#
-   [[32c4fc3b|Installing `pdf-tools` elisp code]]#
