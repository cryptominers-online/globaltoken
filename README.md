Globaltoken integration/staging tree
================================

--> Globaltoken has no offical Website yet. <--
You can visit for more informations the Bitcointalk Thread here: https://bitcointalk.org/index.php?topic=1706793

Copyright (c) 2017 Globaltoken Developers

What is Globaltoken?
----------------

Globaltoken is an experimental new digital currency that enables instant payments to
anyone, anywhere in the world. Globaltoken uses peer-to-peer technology to operate
with no central authority: managing transactions and issuing money are carried
out collectively by the network. Globaltoken is also the name of the open source
software which enables the use of this currency.

For more information, as well as an immediately useable, binary version of
the Globaltoken client software, see the actual Bitcointalk thread: https://bitcointalk.org/index.php?topic=1706793

License
-------

Globaltoken is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.

Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the Globaltoken
development team members simply pulls it.

If it is a *more complicated or potentially controversial* change, then the patch
submitter will be asked to start a discussion (if they haven't already) on the
[mailing list](http://sourceforge.net/mailarchive/forum.php?forum_name=globaltoken-development).

The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't
match the project's coding conventions (see `doc/coding.md`) or are
controversial.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/globaltoken/globaltoken/tags) are created
regularly to indicate new official, stable release versions of Globaltoken.

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test. Please be patient and help out, and
remember this is a security-critical project where any mistake might cost people
lots of money.

If there are Problems on Linux to compile pls use this command:

	chmod 755 src/leveldb/build_detect_platform

### Automated Testing

Developers are strongly encouraged to write unit tests for new code, and to
submit new unit tests for old code.

Unit tests for the core code are in `src/test/`. To compile and run them:

    cd src; make -f makefile.unix test

Unit tests for the GUI code are in `src/qt/test/`. To compile and run them:

    qmake BITCOIN_QT_TEST=1 -o Makefile.test globaltoken-qt.pro
    make -f Makefile.test
    ./globaltoken-qt_test

Every pull request is built for both Windows and Linux on a dedicated server,
and unit and sanity tests are automatically run. The binaries produced may be
used for manual QA testing — a link to them will appear in a comment on the
pull request posted by [GlobaltokenPullTester](https://github.com/GlobaltokenPullTester). See https://github.com/TheBlueMatt/test-scripts
for the build/test scripts.

### Manual Quality Assurance (QA) Testing

Large changes should have a test plan, and should be tested by somebody other
than the developer who wrote the code.

See https://github.com/globaltoken/QA/ for how to create a test plan.
