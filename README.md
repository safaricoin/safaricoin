Safaricoin
================================

http://www.funtrench.com

Copyright (c) 2009-2013 Bitcoin Developers
Copyright (c) 2013-TODAY Safaricoin Developers

What is Safaricoin?
----------------

Safaricoin is a version of Bitcoin using the Scrypt algorithm as a proof-of-work algorithm.
 - 1 minute block targets
 - subsidy halves in 840k blocks
 - ~50 million total coins

The rest is almost the same as Litecoin.
 - 200 coins per block
 - 2016 blocks to retarget difficulty

Safaricoin is intended as an intermediate currency for mobile money transfers within East Africa,
with capacity to intergrate seamlessly with the global cryptocoin economy for international
transfers. As such, the coins are distributed via IPO to the agents in the network and mining is
not the primary way of getting new coins.

Transaction fees will be set as a small percentage of the value sent and fixed.

For more information, as well as an immediately useable, binary version of
the Safaricoin client sofware, see http://www.funtrench.com.

License
-------

Safaricoin is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.

Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the Safaricoin
development team members simply pulls it.

If it is a *more complicated or potentially controversial* change, then the patch
submitter will be asked to start a discussion (if they haven't already) on the
[mailing list](http://sourceforge.net/mailarchive/forum.php?forum_name=safaricoin-development).

The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't
match the project's coding conventions (see `doc/coding.txt`) or are
controversial.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/safaricoin/safaricoin/tags) are created
regularly to indicate new official, stable release versions of Safaricoin.

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test. Please be patient and help out, and
remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write unit tests for new code, and to
submit new unit tests for old code.

Unit tests for the core code are in `src/test/`. To compile and run them:

    cd src; make -f makefile.unix test

Unit tests for the GUI code are in `src/qt/test/`. To compile and run them:

    qmake SAFARICOIN_QT_TEST=1 -o Makefile.test safaricoin-qt.pro
    make -f Makefile.test
    ./safaricoin-qt_test