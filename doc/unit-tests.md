Compiling/running globaltokend unit tests
------------------------------------

globaltokend unit tests are in the `src/test/` directory; they
use the Boost::Test unit-testing framework.

To compile and run the tests:

	cd src
	make -f makefile.unix test_globaltoken  # Replace makefile.unix if you're not on unix
	./test_globaltoken   # Runs the unit tests

If all tests succeed the last line of output will be:
`*** No errors detected`

To add more tests, add `BOOST_AUTO_TEST_CASE` functions to the existing
.cpp files in the test/ directory or add new .cpp files that
implement new BOOST_AUTO_TEST_SUITE sections (the makefiles are
set up to add test/*.cpp to test_globaltoken automatically).


Compiling/running Globaltoken-Qt unit tests
---------------------------------------

Globaltoken-Qt unit tests are in the src/qt/test/ directory; they
use the Qt unit-testing framework.

To compile and run the tests:

	qmake globaltoken-qt.pro BITCOIN_QT_TEST=1
	make
	./globaltoken-qt_test

To add more tests, add them to the `src/qt/test/` directory,
the `src/qt/test/test_main.cpp` file, and globaltoken-qt.pro.
