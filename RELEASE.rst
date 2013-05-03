-------------
Release notes
-------------


mgunit 1.4
----------

* Fix for test cases with no valid tests.


mgunit 1.3
----------
Released 12 February 2013

* Added optional OUTPUT keyword to tests which, if present and set during the
  the test, is echoed to the output.

* Added utilities to help test GUI applications.

* Updated "Using mgunit" documentation.

* Adding error_is_skip.pro batch file with optional variable MGUNIT_SKIP_MSG
  which can be set prior to including error_is_skip.pro to a message that will
  be used if an error causes the skip.

* Updated look for HTML output.


mgunit 1.2
----------
Released 7 July 2011

* Added FAILURES_ONLY keyword to display only failed tests.

* Simplified and improved user-level API documentation.

* Added VERSION keyword to report mgunit version.


mgunit 1.1
----------
Released 22 February 2010

* Added an extra argument to ASSERT which can be inserted into the
  message via C-style format codes.

* Added XML and JUnit output formats (and corresponding XML and JUNIT keywords
  to MGUNIT to turn them on).
  
* Added ability for a test to determine if it should count in the
  final results tally, i.e., if it is "skipped". Use the SKIP keyword
  of ASSERT to skip a test instead of failing it if the condition is
  not met.

* Fixed memory leak.

  
mgunit 1.0
----------
Released 27 April 2009

* Framework for creating pass/fail unit tests with as little overhead and
  boilerplate text as possible. Simply create a new class which inherits from
  MGutTestCase, no init or cleanup methods are necessary unless the test
  requires some setup before it is run. Any function method whose name begins
  with "test" will be executed: it is considered a pass if it returns 1,
  failing if it returns 0 or crashes.

* Suites can automatically gather together many test case classes together if
  the tests follow a simple naming convention: end the test case classname in
  "_ut". In this way, mgunit can run individual test cases or test suites
  aggregating test cases at various levels.

* Several test runners for outputting test results to various formats are
  available; output can be sent to stdout, log files, or html files. In
  addition, there is a GUI test runner that will show results and re-run tests
  with the push of a button (also recompiling tests before running them).

* If there is common setup required for each test method in a test case, a
  setup method can be written. This method will be called before each test
  method (the teardown method will be called after each test method).

* Contains IDL Workbench templates for making it even faster to create new
  test cases/suites.
  
* Keywords to MGUNIT to retrieve the number of passing and failing tests.

* Color output to the terminal window when possible.

* Shell script to run mgunit from the UNIX command line.
