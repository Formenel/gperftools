These tools are for use by developers so that they can create more robust applications. Especially of use to those developing multi-threaded applications in C++ with templates. Includes TCMalloc, heap-checker, heap-profiler and cpu-profiler.

Downloads:

  * [gperftools-2.4.tar.gz](https://googledrive.com/host/0B6NtGsLhIcf7MWxMMF9JdTN3UVk/gperftools-2.4.tar.gz)
  * [gperftools-2.4.zip](https://googledrive.com/host/0B6NtGsLhIcf7MWxMMF9JdTN3UVk/gperftools-2.4.zip)
  * [gperftools-2.3.90.tar.gz](https://googledrive.com/host/0B6NtGsLhIcf7MWxMMF9JdTN3UVk/gperftools-2.3.90.tar.gz) (aka 2.4rc)
  * [gperftools-2.3.90.zip](https://googledrive.com/host/0B6NtGsLhIcf7MWxMMF9JdTN3UVk/gperftools-2.3.90.zip) (aka 2.4rc)
  * [gperftools-2.3.tar.gz](https://googledrive.com/host/0B6NtGsLhIcf7MWxMMF9JdTN3UVk/gperftools-2.3.tar.gz)
  * [gperftools-2.3.zip](https://googledrive.com/host/0B6NtGsLhIcf7MWxMMF9JdTN3UVk/gperftools-2.3.zip)
  * [gperftools-2.2.1.tar.gz](https://googledrive.com/host/0B6NtGsLhIcf7MWxMMF9JdTN3UVk/gperftools-2.2.1.tar.gz)
  * [gperftools-2.2.1.zip](https://googledrive.com/host/0B6NtGsLhIcf7MWxMMF9JdTN3UVk/gperftools-2.2.1.zip)
  * [gperftools-2.2.tar.gz](https://googledrive.com/host/0B6NtGsLhIcf7MWxMMF9JdTN3UVk/gperftools-2.2.tar.gz)
  * [gperftools-2.2.zip](https://googledrive.com/host/0B6NtGsLhIcf7MWxMMF9JdTN3UVk/gperftools-2.2.zip)
  * [gperftools-2.1.tar.gz](https://googledrive.com/host/0B6NtGsLhIcf7MWxMMF9JdTN3UVk/gperftools-2.1.tar.gz)
  * [gperftools-2.1.zip](https://googledrive.com/host/0B6NtGsLhIcf7MWxMMF9JdTN3UVk/gperftools-2.1.zip)

Recent news:

## 10 Jan 2015 ##

gperftools 2.4 is out! The code is exactly same as 2.4rc.


## 28 Dec 2014 ##

gperftools 2.4rc is out!

Downloads:

  * https://googledrive.com/host/0B6NtGsLhIcf7MWxMMF9JdTN3UVk/gperftools-2.3.90.zip
  * https://googledrive.com/host/0B6NtGsLhIcf7MWxMMF9JdTN3UVk/gperftools-2.3.90.tar.gz


Here are changes since 2.3:

  * enabled aggressive decommit option by default. It was found to significantly improve memory fragmentation with negligible impact on performance. (Thanks to investigation work performed by Adhemerval Zanella)

  * added ./configure flags for tcmalloc pagesize and tcmalloc allocation alignment. Larger page sizes have been reported to improve performance occasionally. (Patch by Raphael Moreira Zinsly)

  * sped-up hot-path of malloc/free. By about 5% on static library and about 10% on shared library. Mainly due to more efficient checking of malloc hooks.

  * improved accuracy of stacktrace capturing in cpu profiler (due to issue found by Arun Sharma). As part of that issue pprof's handling of cpu profiles was also improved.


## 7 Dec 2014 ##

gperftools 2.3 is out!

Downloads:

  * https://googledrive.com/host/0B6NtGsLhIcf7MWxMMF9JdTN3UVk/gperftools-2.3.zip
  * https://googledrive.com/host/0B6NtGsLhIcf7MWxMMF9JdTN3UVk/gperftools-2.3.tar.gz


Here are changes since 2.3rc:

  * ([issue 658](https://code.google.com/p/gperftools/issues/detail?id=658)) correctly close socketpair fds on failure (patch by glider)

  * libunwind integration can be disabled at configure time (patch by Raphael Moreira Zinsly)

  * libunwind integration is disabled by default for ppc64 (patch by Raphael Moreira Zinsly)

  * libunwind integration is force-disabled for OSX. It was not used by default anyways. Fixes compilation issue I saw.

## 2 Nov 2014 ##

gperftools 2.3rc is out!

Downloads:

  * https://googledrive.com/host/0B6NtGsLhIcf7MWxMMF9JdTN3UVk/gperftools-2.2.90.zip
  * https://googledrive.com/host/0B6NtGsLhIcf7MWxMMF9JdTN3UVk/gperftools-2.2.90.tar.gz

Most small improvements in this release were made to pprof tool.

New experimental Linux-only (for now) cpu profiling mode is a notable big improvement.

Here are notable changes since 2.2.1:

  * ([issue 631](https://code.google.com/p/gperftools/issues/detail?id=631)) fixed debugallocation miscompilation on mmap-less platforms (courtesy of user iamxujian)

  * ([issue 630](https://code.google.com/p/gperftools/issues/detail?id=630)) reference to wrong PROFILE (vs. correct CPUPROFILE) environment variable was fixed (courtesy of WenSheng He)

  * pprof now has option to display stack traces in output for heap checker (courtesy of Michael Pasieka)

  * ([issue 636](https://code.google.com/p/gperftools/issues/detail?id=636)) pprof web command now works on mingw

  * ([issue 635](https://code.google.com/p/gperftools/issues/detail?id=635)) pprof now handles library paths that contain spaces (courtesy of user mich...@sebesbefut.com)

  * ([issue 637](https://code.google.com/p/gperftools/issues/detail?id=637)) pprof now has an option to not strip template arguments (patch by jiakai)

  * ([issue 644](https://code.google.com/p/gperftools/issues/detail?id=644)) possible out-of-bounds access in GetenvBeforeMain was fixed (thanks to user abyss.7)

  * ([issue 641](https://code.google.com/p/gperftools/issues/detail?id=641)) pprof now has an option --show\_addresses (thanks to user yurivict). New option prints instruction address in addition to function name in stack traces

  * ([issue 646](https://code.google.com/p/gperftools/issues/detail?id=646)) pprof now works around some issues of addr2line reportedly when DWARF v4 format is used (patch by Adam McNeeney)

  * ([issue 645](https://code.google.com/p/gperftools/issues/detail?id=645)) heap profiler exit message now includes remaining memory allocated info (patch by user yurivict)

  * pprof code that finds location of /proc/pid/maps in cpu profile files is now fixed (patch by Ricardo M. Correia)

  * ([issue 654](https://code.google.com/p/gperftools/issues/detail?id=654)) pprof now handles "split text segments" feature of Chromium for Android (patch by simonb)

  * ([issue 655](https://code.google.com/p/gperftools/issues/detail?id=655)) potential deadlock on windows caused by early call to getenv in malloc initialization code was fixed (bug reported and fix proposed by user zndmitry)

  * incorrect detection of arm 6zk instruction set support (-mcpu=arm1176jzf-s) was fixed. (Reported by pedronavf on old issue-493)

  * new cpu profiling mode on Linux is now implemented. It sets up separate profiling timers for separate threads. Which improves accuracy of profiling on Linux a lot. It is off by default. And is enabled if both librt.f is loaded and CPUPROFILE\_PER\_THREAD\_TIMERS environment variable is set. But note that all threads need to be registered via ProfilerRegisterThread.


## 21 Jun 2014 ##

gperftools 2.2.1 is out!

Downloads:

  * https://googledrive.com/host/0B6NtGsLhIcf7MWxMMF9JdTN3UVk/gperftools-2.2.1.zip
  * https://googledrive.com/host/0B6NtGsLhIcf7MWxMMF9JdTN3UVk/gperftools-2.2.1.tar.gz

Here's list of fixes:

  * [issue 626](https://code.google.com/p/gperftools/issues/detail?id=626) was closed. Which fixes initialization of statically linked tcmalloc.

  * [issue 628](https://code.google.com/p/gperftools/issues/detail?id=628) was closed. It adds missing header file into source tarball. This fixes for compilation on PPC Linux.



## 3 May 2014 ##

gperftools 2.2 is out!

Downloads:

  * https://googledrive.com/host/0B6NtGsLhIcf7MWxMMF9JdTN3UVk/gperftools-2.2.zip
  * https://googledrive.com/host/0B6NtGsLhIcf7MWxMMF9JdTN3UVk/gperftools-2.2.tar.gz


Here are notable changes since 2.2rc:

  * [issue 620](https://code.google.com/p/gperftools/issues/detail?id=620) (crash on windows when c runtime dll is reloaded) was fixed

## 19 Apr 2014 ##

gperftools 2.2rc is out! (Note that downloads are now served via google drive. Get it here: https://drive.google.com/folderview?id=0B6NtGsLhIcf7MWxMMF9JdTN3UVk)

Direct links:

  * [gperftools-2.1.90.zip](https://drive.google.com/uc?export=download&id=0B6NtGsLhIcf7aXJQR0d1ME0zNUU)
  * [gperftools-2.1.90.tar.gz](https://docs.google.com/uc?export=download&id=0B6NtGsLhIcf7b1E3RlVMelc3dW8)

Here are notable changes since 2.1:

  * a number of fixes for a number compilers and platforms. Notably Visual Studio 2013, recent mingw with c++ threads and some OSX fixes.

  * we now have mips and mips64 support! (courtesy of Jovan Zelincevic, Jean Lee, user xiaoyur347 and others)

  * we now have aarch64 (aka arm64) support! (contributed by Riku Voipio)

  * there's now support for ppc64-le (by Raphael Moreira Zinsly and Adhemerval Zanella)

  * there's now some support of uclibc (contributed by user xiaoyur347)

  * google/ headers will now give you deprecation warning. They are deprecated since 2.0

  * there's now new api: tc\_malloc\_skip\_new\_handler (ported from chromium fork)

  * [issue 557](https://code.google.com/p/gperftools/issues/detail?id=557): added support for dumping heap profile via signal (by Jean Lee)

  * [issue 567](https://code.google.com/p/gperftools/issues/detail?id=567): Petr Hosek contributed SysAllocator support for windows

  * Joonsoo Kim contributed several speedups for central freelist code

  * TCMALLOC\_MAX\_TOTAL\_THREAD\_CACHE\_BYTES environment variable now works

  * configure scripts are now using AM\_MAINTAINER\_MODE. It'll only affect folks who modify source from .tar.gz and want automake to automatically rebuild Makefile-s. See automake documentation for that.

  * [issue 586](https://code.google.com/p/gperftools/issues/detail?id=586): detect main executable even if PIE is active (based on patch by user themastermind1). Notably, it fixes profiler use with ruby.

  * there is now support for switching backtrace capturing method at runtime (via TCMALLOC\_STACKTRACE\_METHOD and TCMALLOC\_STACKTRACE\_METHOD\_VERBOSE environment variables)

  * there is new backtrace capturing method using -finstrument-functions prologues contributed by user xiaoyur347

  * few cases of crashes/deadlocks in profiler were addressed. See (famous) issue-66, [issue 547](https://code.google.com/p/gperftools/issues/detail?id=547) and [issue 579](https://code.google.com/p/gperftools/issues/detail?id=579).

  * [issue 464](https://code.google.com/p/gperftools/issues/detail?id=464) (memory corruption in debugalloc's realloc after memallign) is now fixed

  * tcmalloc is now able to release memory back to OS on windows ([issue 489](https://code.google.com/p/gperftools/issues/detail?id=489)). The code was ported from chromium fork (by a number of authors).

  * Together with [issue 489](https://code.google.com/p/gperftools/issues/detail?id=489) we ported chromium's "aggressive decommit" mode. In this mode (settable via malloc extension and via environment variable TCMALLOC\_AGGRESSIVE\_DECOMMIT), free pages are returned back to OS immediately.

  * MallocExtension::instance() is now faster (based on patch by Adhemerval Zanella)

  * [issue 610](https://code.google.com/p/gperftools/issues/detail?id=610) (hangs on windows in multibyte locales) is now fixed

The following people helped with ideas or patches (based on git log, some contributions purely in bugtracker might be missing): Andrew C. Morrow, yurivict, Wang YanQing, Thomas Klausner, davide.italiano@10gen.com, Dai MIKURUBE, Joon-Sung Um, Jovan Zelincevic, Jean Lee, Petr Hosek, Ben Avison, drussel, Joonsoo Kim, Hannes Weisbach, xiaoyur347, Riku Voipio, Adhemerval Zanella, Raphael Moreira Zinsly


## 30 July 2013 ##

gperftools 2.1 is out!

Downloads:

  * https://googledrive.com/host/0B6NtGsLhIcf7MWxMMF9JdTN3UVk/gperftools-2.1.zip
  * https://googledrive.com/host/0B6NtGsLhIcf7MWxMMF9JdTN3UVk/gperftools-2.1.tar.gz


Just few fixes where merged after rc. Most notably:

  * Some fixes for debug allocation on POWER/Linux

## 20 July 2013 ##

gperftools 2.1rc is out!

As a result of more than a year of contributions we're ready for 2.1
release.

But before making that step I'd like to create RC and make sure people
have chance to test it.

Here are notable changes since 2.0:

  * fixes for building on newer platforms. Notably, there's now initial support for x32 ABI (--enable-minimal only at this time)

  * new getNumericProperty stats for cache sizes

  * added HEAP\_PROFILER\_TIME\_INTERVAL variable (see documentation)

  * added environment variable to control heap size (TCMALLOC\_HEAP\_LIMIT\_MB)

  * added environment variable to disable release of memory back to OS (TCMALLOC\_DISABLE\_MEMORY\_RELEASE)

  * cpu profiler can now be switched on and off by sending it a signal (specified in CPUPROFILESIGNAL)

  * ([issue 491](https://code.google.com/p/gperftools/issues/detail?id=491)) fixed race-ful spinlock wake-ups

  * ([issue 496](https://code.google.com/p/gperftools/issues/detail?id=496)) added some support for fork-ing of process that is using tcmalloc

  * ([issue 368](https://code.google.com/p/gperftools/issues/detail?id=368)) improved memory fragmentation when large chunks of memory are allocated/freed

## 06 February 2012 ##

Hello from your new maintainer. I am hoping that the growing community
of the project formerly know as `google-perftools`, is going to keep me
busy with patch work. I strongly encourage everyone to dedicate some
time and expertise where you can so that we can continue to build out
features and support for `gperftools`. The amount of time these
performance tools have saved me over the last year in debugging memory
leaks and troubleshooting performance issues, has far exceeded the time
I have given to make improvements. If you are familiar with MIPS or OSX
porting and want to contribute, I have a few issues that need to be taken
care of :)

As my background with `gperftools` is still relatively limited, I will
likely be doing some house cleaning activities over the next few months
to broaden my familiarity. In the mean time, I will do what I can to
answer questions, triage new issues, and organize patch work for release.
Ideally I would like to push out a patch every 3-4 months provided that
it is justified.

-Dave

## 03 February 2012 ##

I've just released gperftools 2.0!

The `google-perftools` project has been renamed to `gperftools`.  I
(csilvers) am stepping down as maintainer, to be replaced by
David Chappelle.  Welcome to the team, David!  David has been an
an active contributor to perftools in the past -- in fact, he's the
only person other than me that already has commit status.  I am
pleased to have him take over as maintainer.

I have both renamed the project (the Google Code site renamed a few
weeks ago), and bumped the major version number up to 2, to reflect
the new community ownership of the project.  Almost all the
[changes](http://gperftools.googlecode.com/svn/tags/gperftools-2.0/ChangeLog)
are related to the renaming.

The main functional change from google-perftools 1.10 is that
I've renamed the `google/` include-directory to be `gperftools/`
instead.  New code should `#include <gperftools/tcmalloc.h>`/etc.
(Most users of perftools don't need any perftools-specific includes at
all, so this is mostly directed to "power users.")  I've kept the old
names around as forwarding headers to the new, so `#include
<google/tcmalloc.h>` will continue to work.

(The other functional change which I snuck in is getting rid of some
bash-isms in one of the unittest driver scripts, so it could run on
Solaris.)

Note that some internal names still contain the text `google`, such as
the `google_malloc` internal linker section.  I think that's a
trickier transition, and can happen in a future release (if at all).


### 31 January 2012 ###

I've just released perftools 1.10

There is an API-incompatible change: several of the methods in the
`MallocExtension` class have changed from taking a `void*` to taking a
`const void*`.  You should not be affected by this API change
unless you've written your own custom malloc extension that derives
from `MallocExtension`, but since it is a user-visible change, I have
upped the `.so` version number for this release.

This release focuses on improvements to linux-syscall-support.h,
including ARM and PPC fixups and general cleanups.  I hope this will
magically fix an array of bugs people have been seeing.

There is also exciting news on the porting front, with support for
patching win64 assembly contributed by IBM Canada!  This is an
important step -- perhaps the most difficult -- to getting perftools
to work on 64-bit windows using the patching technique (it doesn't
affect the libc-modification technique).  `premable_patcher_test` has
been added to help test these changes; it is meant to compile under
x86\_64, and won't work under win32.

For the full list of changes, including improved `HEAP_PROFILE_MMAP`
support, see the
[ChangeLog](http://gperftools.googlecode.com/svn/tags/google-perftools-1.10/ChangeLog).


### 24 January 2011 ###

The `google-perftools` Google Code page has been renamed to
`gperftools`, in preparation for the project being renamed to
`gperftools`.  In the coming weeks, I'll be stepping down as
maintainer for the perftools project, and as part of that Google is
relinquishing ownership of the project; it will now be entirely
community run.  The name change reflects that shift.  The 'g' in
'gperftools' stands for 'great'. :-)

### 23 December 2011 ###

I've just released perftools 1.9.1

I missed including a file in the tarball, that is needed to compile on
ARM.  If you are not compiling on ARM, or have successfully compiled
perftools 1.9, there is no need to upgrade.


### 22 December 2011 ###

I've just released perftools 1.9

This change has a slew of improvements, from better ARM and freebsd
support, to improved performance by moving some code outside of locks,
to better pprof reporting of code with overloaded functions.

The full list of changes is in the
[ChangeLog](http://google-perftools.googlecode.com/svn/tags/google-perftools-1.9/ChangeLog).

Note some of these changes -- particularly the ARM changes -- are on systems that I don't have available for testing, so please let me know if you see any problems with them!


### 26 August 2011 ###

I've just released perftools 1.8.3

The star-crossed 1.8 series continues; in 1.8.1, I had accidentally
removed some code that was needed for FreeBSD.  (Without this code
many apps would crash at startup.)  This release re-adds that code.
If you are not on FreeBSD, or are using FreeBSD with perftools 1.8 or
earlier, there is no need to upgrade.

### 11 August 2011 ###

I've just released perftools 1.8.2

I was incorrectly calculating the patch-level in the configuration
step, meaning the `TC_VERSION_PATCH` `#define` in `tcmalloc.h` was wrong.
Since the testing framework checks for this, it was failing.  Now it
should work again.  This time, I was careful to re-run my tests after
upping the version number. :-)

If you don't care about the `TC_VERSION_PATCH` `#define`, there's no
reason to upgrade.

### 26 July 2011 ###

I've just released perftools 1.8.1

I was missing an #include that caused the build to break under some
compilers, especially newer gcc's, that wanted it.  This only affects
people who build from source, so only the .tar.gz file is updated from
perftools 1.8.  If you didn't have any problems compiling perftools
1.8, there's no reason to upgrade.

### 15 July 2011 ###

I've just released perftools 1.8

Of the many changes in this release, a good number pertain to porting.
I've revamped OS X support to use the malloc-zone framework; it should
now Just Work to link in tcmalloc, without needing
`DYLD_FORCE_FLAT_NAMESPACE` or the like.  (This is a pretty major
change, so please feel free to report feedback at
google-perftools@googlegroups.com.)  64-bit Windows support is also
improved, as is ARM support, and the hooks are in place to improve
FreeBSD support as well.

On the other hand, I'm seeing hanging tests on Cygwin.  I see the same
hanging even with (the old) perftools 1.7, so I'm guessing this is
either a problem specific to my Cygwin installation, or nobody is
trying to use perftools under Cygwin.  If you can reproduce the
problem, and even better have a solution, you can report it at
google-perftools@googlegroups.com.

Internal changes include several performance and space-saving tweaks.
One is user-visible (but in "stealth mode", and otherwise
undocumented): you can compile with `-DTCMALLOC_SMALL_BUT_SLOW`.  In
this mode, tcmalloc will use less memory overhead, at the cost of
running (likely not noticeably) slower.

There are many other changes as well, too numerous to recount here,
but present in the
[ChangeLog](http://google-perftools.googlecode.com/svn/tags/google-perftools-1.8/ChangeLog).

### 7 February 2011 ###

Thanks to endlessr..., who
[identified](http://code.google.com/p/google-perftools/issues/detail?id=307)
why some tests were failing under MSVC 10 in release mode.  The problem was not
with tcmalloc but with the test itself, which made some assumptions that broke
under some aggressive (or possibly buggy) optimizations used in MSVC 10.
I've fixed the test in [svn](http://code.google.com/p/google-perftools/source/checkout),
but even if using the 1.7 .zip file, feel free to compile perftools under MSVC 10.

### 4 February 2011 ###

I've just released perftools 1.7

I apologize for the delay since the last release; so many great new
patches and bugfixes kept coming in (and are still coming in; I also
apologize to those folks who have to slip until the next release).  I
picked this arbitrary time to make a cut.

Among the many new features in this release is a multi-megabyte
reduction in the amount of tcmalloc overhead uder x86\_64, improved
performance in the case of contention, and many many bugfixes,
especially architecture-specific bugfixes.  See the
[ChangeLog](http://google-perftools.googlecode.com/svn/tags/google-perftools-1.7/ChangeLog)
for full details.

One architecture-specific change of note is added comments in the
[README](http://google-perftools.googlecode.com/svn/tags/perftools-1.7/README)
for using tcmalloc under OS X.  I'm trying to get my head around the
exact behavior of the OS X linker, and hope to have more improvements
for the next release, but I hope these notes help folks who have been
having trouble with tcmalloc on OS X.

**Windows users**: I've heard reports that some unittests fail on
Windows when compiled with MSVC 10 in Release mode.  All tests pass in
Debug mode.  I've not heard of any problems with earlier versions of
MSVC.  I don't know if this is a problem with the runtime patching (so
the static patching discussed in README\_windows.txt will still work),
a problem with perftools more generally, or a bug in MSVC 10.  Anyone
with windows expertise that can debug this, I'd be glad to hear from!


### 5 August 2010 ###

I've just released perftools 1.6

This version also has a large number of minor changes, including
support for `malloc_usable_size()` as a glibc-compatible alias to
`malloc_size()`, the addition of SVG-based output to `pprof`, and
experimental support for tcmalloc large pages, which may speed up
tcmalloc at the cost of greater memory use.  To use tcmalloc large
pages, see the
[INSTALL file](http://google-perftools.googlecode.com/svn/tags/perftools-1.6/INSTALL); for all changes, see the
[ChangeLog](http://google-perftools.googlecode.com/svn/tags/perftools-1.6/ChangeLog).

OS X NOTE: improvements in the profiler unittest have turned up an OS
X issue: in multithreaded programs, it seems that OS X often delivers
the profiling signal (from sigitimer()) to the main thread, even when
it's sleeping, rather than spawned threads that are doing actual work.
If anyone knows details of how OS X handles SIGPROF events (from
setitimer) in threaded programs, and has insight into this problem,
please send mail to google-perftools@googlegroups.com.

To see if you're affected by this, look for profiling time that pprof
attributes to `___semwait_signal`.  This is work being done in other
threads, that is being attributed to sleeping-time in the main thread.


### 20 January 2010 ###

I've just released perftools 1.5

This version has a slew of changes, leading to somewhat faster performance and improvements in portability.  It adds features like `ITIMER_REAL` support to the cpu
profiler, and `tc_set_new_mode` to mimic the windows function of the same name.
Full details are in the [ChangeLog](http://google-perftools.googlecode.com/svn/tags/perftools-1.5/ChangeLog).

### 11 September 2009 ###

I've just released perftools 1.4

The major change this release is the addition of a debugging malloc library!
If you link with `libtcmalloc_debug.so` instead of `libtcmalloc.so` (and likewise
for the `minimal` variants) you'll get a debugging malloc, which will catch
double-frees, writes to freed data, `free`/`delete` and `delete`/`delete[]` mismatches,
and even (optionally) writes past the end of an allocated block.

We plan to do more with this library in the future, including supporting it on Windows,
and adding the ability to use the debugging library with your default malloc in addition to using it with tcmalloc.

There are also the usual complement of bug fixes, documented in the ChangeLog, and a
few minor user-tunable knobs added to components like the system allocator.


### 9 June 2009 ###

I've just released perftools 1.3

Like 1.2, this has a variety of bug fixes, especially related to the Windows build.
One of my bugfixes is to undo the weird `ld -r` fix to `.a` files that I introduced in perftools 1.2: it caused problems on too many platforms.  I've reverted back to normal `.a` files.  To work around the original problem that prompted the `ld -r` fix, I now provide `libtcmalloc_and_profiler.a`, for folks who want to link in both.

The most interesting API change is that I now not only override `malloc`/`free`/etc, I also expose them via a unique set of symbols: `tc_malloc`/`tc_free`/etc.  This enables clients to write their own memory wrappers that use tcmalloc:
```
   void* malloc(size_t size) { void* r = tc_malloc(size); Log(r); return r; }
```


### 17 April 2009 ###

I've just released perftools 1.2.

This is mostly a bugfix release.  The major change is internal: I have a new system for creating packages, which allows me to create 64-bit packages.  (I still don't do that for perftools, because there is still no great 64-bit solution, with libunwind still giving problems and --disable-frame-pointers not practical in every environment.)

Another interesting change involves Windows: a [new patch](http://code.google.com/p/google-perftools/issues/detail?id=126) allows users to choose to override malloc/free/etc on Windows rather than patching, as is done now.  This can be used to create custom CRTs.

My fix for this [bug involving static linking](http://groups.google.com/group/google-perftools/browse_thread/thread/1ff9b50043090d9d/a59210c4206f2060?lnk=gst&q=dynamic#a59210c4206f2060) ended up being to make libtcmalloc.a and libperftools.a a big .o file, rather than a true `ar` archive.  This should not yield any problems in practice -- in fact, it should be better, since the heap profiler, leak checker, and cpu profiler will now all work even with the static libraries -- but if you find it does, please file a bug report.

Finally, the profile\_handler\_unittest provided in the perftools testsuite (new in this release) is failing on FreeBSD.  The end-to-end test that uses the profile-handler is passing, so I suspect the problem may be with the test, not the perftools code itself.  However, I do not know enough about how itimers work on FreeBSD to be able to debug it.  If you can figure it out, please let me know!

### 11 March 2009 ###

I've just released perftools 1.1!

It has many changes since perftools 1.0 including

  * Faster performance due to dynamically sized thread caches
  * Better heap-sampling for more realistic profiles
  * Improved support on Windows (MSVC 7.1 and cygwin)
  * Better stacktraces in linux (using VDSO)
  * Many bug fixes and feature requests

Note: if you use the CPU-profiler with applications that fork without
doing an exec right afterwards, please see the README.  Recent testing
has shown that profiles are unreliable in that case.  The problem has
existed since the first release of perftools.  We expect to have a fix
for perftools 1.2.  For more details, see
[issue 105](http://code.google.com/p/google-perftools/issues/detail?id=105).

Everyone who uses perftools 1.0 is encouraged to upgrade to perftools
1.1.  If you see any problems with the new release, please file a bug
report at http://code.google.com/p/google-perftools/issues/list.

Enjoy!