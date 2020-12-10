git2cl
======

This is a quick'n'dirty tool to convert git logs to GNU ChangeLog
format.

The tool invokes 'git log' internally unless you pipe a log to it.
Thus, typically you would use it as follows:

...........................................................................
jas@mocca:~/src/libtasn1$ git2cl > ChangeLog
jas@mocca:~/src/libtasn1$
...........................................................................

If you don't want git2cl to invoke git log internally, you can use it
as a pipe.  It needs a git log generated with --pretty --numstat and
--summary.  You can use it as follows:

...........................................................................
jas@mocca:~/src/libtasn1$ git log --pretty --numstat --summary | ~/src/git2cl/git2cl > ChangeLog
jas@mocca:~/src/libtasn1$
...........................................................................

The output format is specified by:

link:http://www.gnu.org/prep/standards/html_node/Change-Logs.html[]

My inspiration for writing this tool was the
link:http://www.red-bean.com/cvs2cl/[cvs2cl] tool, which I have been
using in several projects.  Replacing it was necessary to seriously
consider switching from CVS to GIT for my projects.

The canonical home page for git2cl is:
link:http://josefsson.org/git2cl/[] and its repository can be found at
link:http://repo.or.cz/w/git2cl.git[].

Credits
-------

Luis Mondesi contributed several improvements.

Support
-------

Try talking to mailto:simon@josefsson.org[Simon Josefsson].

License
-------
- SPDX-License-Identifier: GPL-2.0-or-later

``` text
git2cl is free software; you can redistribute it and/or modify it
under the terms of the GNU General Public License as published by
the Free Software Foundation; either version 2, or (at your option)
any later version.

git2cl is distributed in the hope that it will be useful, but
WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU
General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
```
