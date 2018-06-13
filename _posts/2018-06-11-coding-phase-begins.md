---
layout: post
title: "GSoC '18 Post #2: `pytest` over `unittest`"
date: 2018-06-14 01:57:20 +0530
description: Coding phase of Google Summer of Code 2018 begins.
img: coala.png
tags: [GSoC, coala, coding-phase]
---

## What is unit testing ?

Unit testing involves breaking your program into pieces and subjecting each
piece into a series of tests.

Usually, tests are run as separate programs, but the method of testing varies,
depending on the language and type of software (GUI, command-line, library).
Tests are usually run periodically, often after every change to the source
code. For details check out the unit testing article in
[Wikipedia](https://en.wikipedia.org/wiki/Unit_testing).

Most languages have [unit testing
frameworks](http://en.wikipedia.org/wiki/List_of_unit_testing_frameworks).
[`pytest`](http://pytest.org/) and
[`unittest`](https://docs.python.org/2/library/unittest.html) are two
testing frameworks used by [coala](https://coala.io).

## [`pytest`](http://pytest.org/) or [`unittest`](https://docs.python.org/3/library/unittest.html) for coala testing API ?

coala uses [`unittest`](https://docs.python.org/3/library/unittest.html)
for testing API but `pytest` has better features which are also discussed in
the issue [coala/coala#3676](https://github.com/coala/coala/issues/3676) and
over gitter channel.

For example, `pytest` fixtures:

Although unittest does allow us to have setup and teardown, pytest extends
this quite a bit. We can add specific code to run:

- at the beginning and end of a module of test code
(setup_module/teardown_module)
- at the beginning and end of a class of test methods
(setup_class/teardown_class)
- alternate style of the class level fixtures (setup/teardown)
- before and after a test function call (setup_function/teardown_function)
- before and after a test method call (setup_method/teardown_method)

Finally, all agreed on using `pytest` for the testing API. Thanks to
[@NiklasMM](https://github.com/NiklasMM).

## BaseTestHelper, A Base Class for All Bears' Tests

After everyone's agreement on pytest, we moved on with the pytest for creating
the base class of bear's tests. [PR #5496](https://github.com/coala/coala/pull/5496).

Now, all BearTestHelpers class will inherit from `BaseTestHelper` class.
Like,
```py
class BaseTestHelper:
    pass

class LocalBearTestHelper(BaseTestHelper):
    pass

class GlobalBearTestHelper(BaseTestHelper):
    pass
```
Go through the [cEP-0027](https://github.com/coala/cEPs/blob/master/cEP-0027.md) for more information.

## LocalBearTestHelper, A Test Helper Class for All Local Bears

coala testing API has a test helper class for simplification of testing of
local bears which supports following methods:
- `check_validity(...)` and `check_invalidity(...)`

    `check_validity` or `check_invalidity(...)` asserts if your bear yields
    any results for a particular check with a list of strings.

- `check_results(...)`

    `check_results` asserts if your bear results match the actual results on
    execution on the command line interface.

- `verify_local_bears(...)`

    `verify_local_bear` asserts that a check of the given lines with the given
    local bear either yields or does not yield any results.

## GlobalBearTestHelper, A Test Helper Class for All Global Bears

coala's testing API does not support global bear test helper till date. This
project will add support for that. Work is going on with full pace. For the
status, do check [PR #5522](https://github.com/coala/coala/pull/5522).

## What lies ahead ?

We are working on testing API by coding, testing and debugging, failing and
succeeding. Till now, the burndown chart looks like:
![GSoC 2018 Burndown-Phase I]({{site.baseurl}}/assets/img/burdown-phase1.png)

I’m working on the GlobalBearTestHelper testing API and I’m likely to complete
it by this week. 

Thanks for stopping by ! Happy coding ! :blush:
