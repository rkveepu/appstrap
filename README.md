appstrap
========

utilitie(s) to bootstrap your app stack

## pmake

[pkgsrc](http://www.pkgsrc.org) where have you been all my life?  So glad
to finally find this from NetBSD.  I wrote a little wrapper for it.

### How to find a package

 1. Find your package in one of these lists.

   * [The complete list of packages](http://ftp.netbsd.org/pub/pkgsrc/current/pkgsrc/README-all.html)
   * [Packages by Category](http://ftp.netbsd.org/pub/pkgsrc/current/pkgsrc/README.html)

 2. Find the directory name on the package `README.html`.  Look for *The package is located in the "xxx/yyy" directory*. xxx/yyy will be a link

 3. Use the directory name as a command line parameter to `pmake`.

For example

```bash
./pmake devel/scmgit-base
```

will install `pkgsrc` if it is not already there; and then install
[git](http://git-scm.com) with all its dependencies into `~/pkg`.

This will install ffmpeg and shibboleth

```bash
./pmake ACCEPTABLE_LICENSES=lame-license ./pmake multimedia/ffmpeg
./pmake www/shibboleth-sp
```

Works on the SUSE VMs I can get from the datacenter.

Note: it is sort of slow the first time because it has to download and
all the source and build all the packages, but I'm going to try to figure
out how to set up a local repository of the packages so that I only have to 
build them once per each of -dev, -stg, and prod.

> ## About pkgsrc

> The NetBSD Packages Collection (pkgsrc) is a framework for building third-party software on NetBSD and other UNIX-like systems, currently containing over 13000 packages. It is used to enable freely available software to be configured and built easily on supported platforms.

It has stable branches that are tagged every quarter of the year, and the curren (2013-05-30) release is their 50th.


# License 

Copyright © 2013, Regents of the University of California
All rights reserved.

Redistribution and use in source and binary forms, with or without 
modification, are permitted provided that the following conditions are met:

- Redistributions of source code must retain the above copyright notice, 
  this list of conditions and the following disclaimer.
- Redistributions in binary form must reproduce the above copyright notice, 
  this list of conditions and the following disclaimer in the documentation 
  and/or other materials provided with the distribution.
- Neither the name of the University of California nor the names of its
  contributors may be used to endorse or promote products derived from this 
  software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" 
AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE 
IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE 
ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT OWNER OR CONTRIBUTORS BE 
LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR 
CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF 
SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS 
INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN 
CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) 
ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE 
POSSIBILITY OF SUCH DAMAGE.
