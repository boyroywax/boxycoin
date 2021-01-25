DOWNLOAD
========

* Boxycoin [CRP] Source code on github https://github.com/boxycoin/boxycoin-core
* Boxycoin [CRP] Download Releases https://github.com/boxycoin/boxycoin-core/releases/
* Algo YeSPoWer 


Useful links
============

* Mining Pool:    http://pool.boxycoin.io fee 0%.
* BlockExplorer:  http://explorer.boxycoin.io/

* RoadMap:        http://boxycoin.io/roadmap/
* Website:        http://boxycoin.io/

* Twitter:        https://twitter.com/boxycoin_io
* Telegram   :    http://t.me/boxycoin
* Telegram/RU:    http://t.me/boxycoinru
* Telegram/ES:    http://t.me/boxycoines
* Telegram/DE:    http://t.me/boxycoinde


Boxycoin Core integration/staging tree
=====================================

* Copyright (c) 2017-2019 Boxycoin Core Developers
* Copyright (c) 2009-2018 Bitcoin Core Developers
* Copyright (c) 2013-2017 Dash Developers (DarkGravityWave3)
* Copyright (c) 2014-2018 Alexander Peslyak (YesPoWer Original)

Development tips and tricks
----------------------------

**compiling for debugging**

Run configure with the --enable-debug option, then make. Or run configure with
CXXFLAGS="-g -ggdb -O0" or whatever debug flags you need.

**debug.log**

If the code is behaving strangely, take a look in the debug.log file in the data directory;
error and debugging message are written there.

The -debug=... command-line option controls debugging; running with just -debug will turn
on all categories (and give you a very large debug.log file).

The Qt code routes qDebug() output to debug.log under category "qt": run with -debug=qt
to see it.

**testnet and regtest modes**

Run with the -testnet option to run with "play boxycoins" on the test network, if you
are testing multi-machine code that needs to operate across the internet.

If you are testing something that can run on one machine, run with the -regtest option.
In regression test mode blocks can be created on-demand; see qa/rpc-tests/ for tests
that run in -regest mode.

**DEBUG_LOCKORDER**

CranePay Core is a multithreaded application, and deadlocks or other multithreading bugs
can be very difficult to track down. Compiling with -DDEBUG_LOCKORDER (configure
CXXFLAGS="-DDEBUG_LOCKORDER -g") inserts run-time checks to keep track of what locks
are held, and adds warning to the debug.log file if inconsistencies are detected.


License
-------

Boxycoin Core is released under the terms of the MIT license. See [COPYING](COPYING) for more
information or see https://opensource.org/licenses/MIT.

Development Process
-------------------

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/boxycoin/boxycoin-core/tags) are created
regularly to indicate new official, stable release versions of CranePay Core.

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test on short notice. Please be patient and help out by testing
other people's pull requests, and remember this is a security-critical project where any mistake might cost people
lots of money.

Translations
------------

Changes to translations as well as new translations can be submitted to
[CranePay Core's crane-locale repository](https://github.com/boxycoin/core-locale).

**Important**: We do not accept translation changes as GitHub pull requests in main repository.

