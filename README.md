### System Requirements
1. brew
1. python 3.7
1. pipenv

### Setup

    make init

### Run

    python main.py

### Test

    make test


## Discussion

### Tests
I would ordinarily put a lot more time into testing the code -- simply ran out of time.

Some important stuff that is not tested includes the Shelf class and orchestration behaviour of Kitchen class.

Also singleton pattern for Kitchen -- I thought it would be a good idea but I'm having second thoughts.

I'm happy the the test coverage for Order -- wrote these first ;-)

### Overflow
I'm assuming y'all meant description of how we handled the "overflow" shelf -- as integer overflow/underflow doesn't seem all that relevant going off the sample data you supplied.

The way I implemented the overflow shelf and handled the difficulties it imposed with computing value was to split out the concept of a order's value into initial_value - total_decay:

    infant_value: this is basically shelf_life in this example but could be different.
    regular_decay: order decay due to sitting on a regular shelf
    overflow_decay: order decay due to sitting on overflow shelf

### Conclusion
Cool. Thanks for the opportunity ;-)