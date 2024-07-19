## What does this do?
A simple function based atomic operations alternative for Arduino

This simple library allows the user to pass any function to `ATOMIC_OPERATION`, which will automatically disable then re-enable interrupts upon execution of the passed function. 

## Why would I use this?
This library basically fulfills the same purpose as ATOMIC_BLOCK(ATOMIC_RESTORESTATE). Instead of defining code inside the atomic operation, however, you pass a function pointer or similar datatype

## How to use?
Pass any function like datatype. Templates will take care of the rest

Example: (using a lambda)

`ATOMIC_OPERATION([&test_var]() -> void { test_var = 1; });`