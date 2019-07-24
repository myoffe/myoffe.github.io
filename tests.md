# Should I write a test for X?

(Also: Should I TDD?)

Every once in a while, I would contemplate this question.
Because really, who really wants to write tests?

To help myself get motivated, I started curating a short list of reasons of why tests are useful.
Usually I'd add a new reason whenever I realized, in retrospective, how tests would have helped me in a certain situation.

So here it is:

* When you break something later in the future and you’ll be super stressed, you’ll get instant feedback on what you broke instead of scratching your head and wasting hours.
* When you change something later, for example a structure of an object hierarchy or some type definitions, the tests will guide you to what changes are exactly needed to make the rest of the code work with the change.
  * Example: Changing the a response object returned by the API.
* When writing the test you will find out subtle but critical bugs or design flaws that otherwise might elude you.
  * If you only test the whole thing after you've done writing the whole feature, and it will fail, it would take you much longer to debug through the parts of the system instead of working with the immediate problem that causes the tests to fail.
* When creating or modifying any functionality that is more than one function, testing each function separately will give you the confidence that you are really done with one part of the change, and then can move on to the next one. Instead of writing a bunch of things that either one of them has a bug, or all of them, or some of them.
* Tests provide faster feedback loops than full system tests. Especially when tests are done with manual steps.
* Writing a test makes you more deliberate - in design and attention to detail - about the expected output of a unit, so you can plan ahead of time instead of making changes as afterthoughts.
* If you pause working on a feature before finishing it, when return to it and run the tests, it will give you an idea of where you were.
  * Breaking down tests into smaller units of functionality improves this even more.
  * Creating "TODO" tests that fail in advance helps it even more.


## Maybe not write tests when
* Production is on fire
* It's for code that's very likely to be thrown out
