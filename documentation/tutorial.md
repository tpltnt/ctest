CTEST Tutorial
==============

example 0: do nothing
---------------------

This example does (almost) nothing. The code for example0.c is
```
#define CTEST_MAIN
#include "ctest.h"

int main(int argc, const char *argv[])
{
    return ctest_main(argc, argv); 
}
```
This source just defines CTEST_MAIN and includes the ctest-header file.
You can compile it by typing ```make example0```. Executing ```./test```
should not report anything besides "RESULTS: 0 tests (0 ok, 0 failed, 0 skipped) ran in 0 ms".