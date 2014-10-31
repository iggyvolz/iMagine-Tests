iMagine-Tests
=============

Here are the tests that should pass for every stable release that follows the iMagine standards.  Test failures should be first reported to the failing test's GitHub repository, but if the test is faulty it should be reported here.

Test Definitions
================
Tests are defined in JSON.  Preferably, the tests should be directly loaded into the program from this repository, but if this is not possible they may be translated into another syntax, either by hand or by computer.

Tests are arranged in test suites.  Each test suite should test a particular feature or bug.  Individual test suites can be enabled or disabled through each program's tester.  Test data should be input into the info.json file, in the following format:
```json
{
    "name"          : "Some Random Test Suite",
    "description"   : "Tests Some Random Thing",
    "related-issue" : "iggyvolz/iMagine-Tests#123",
}
```
Note: Format subject to change.

Inside each test suite is a tests.json file.  The tests are included in this file:
```json
{
    "shortcode" : {
        "description" : "Description of test",
        "code"        : "i.magine(furok)",
        "result"      : ">i.magine(furok)\n_I_: With this animite, I magine Furok!\nFurok:Let the fur fly!",
        "state"       : {
            "_a_" : "furok",
        },
    },
    "etc...",
}
```
Please note that you can use environmental variables in the code, result, and state blocks.  These are surrounded by underscores.  Here is a list of all environmental variables with desired values:
```json
{
    "_i_" : "Current person; change with changeto(), in all lowercase e.g. tony",
    "_I_" : "Current person; change with changeto(), with first letter uppercase e.g. Tony",
    "_a_" : "Current list of animite, all lowercase, comma separated.  No comma after last animite.",
}
```






