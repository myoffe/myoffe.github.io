# Should I write a test for this?

* When I break something later in the future and I’ll be super stressed, I’ll get instant feedback on what I broke instead of scratching my head and wasting hours
* When I change something later, for example a structure of an object hierarchy or some type definitions, the tests will guide me to what changes are exactly needed to make the rest of the code work with the change.
	* Example: Changing the roaming contract structure for simplification of the API
* When writing the test you will find out subtle bugs that otherwise might elude you
	* e.g. roaming data splitting - only when writing the test I found that I started to split from month 1 (=February), and that it probably would not have worked at all. If I tested the whole thing it would fail and it would take me much longer time to debug through instead of working with the immediate problem
* When creating or modifying any functionality that is more than one function, it gives you the confidence that you are really done with one part of the change, and then move on to the next one. Instead of writing a bunch of things that either one of them has a bug, or all of them, or some of them.
* Tests provide faster feedback loops than full system tests. Especially when tests are done with manual steps.
* Writing a test makes me more deliberate, and I give more attention to detail about the expected output of unit, so I can plan ahead instead of adding it later.
* If I stop working on a feature in the middle, running the tests will give me an idea of where I am. Breaking down tests into smaller units of functionality is even better.
