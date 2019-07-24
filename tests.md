# Should I write a test for X?

(Also: Should I TDD?)

Every once in a while, I would contemplate this question.
Because really, who really wants to write tests?

I usually remember that I think that it's a good idea, but I don't always remember *why* it's a good idea.

To remind myself, I started putting my thoughts into a note. In time it turned into the following list of reasons of why tests are useful.

Usually I'd add a new reason in retrospective, when I realized how tests would have helped me at that situation. So here it is.
This is mostly relevant to _new_ code, but may also apply to existing code (and it's easier to write tests for new code).

## Why write tests?

* At some point in time, you, or a team member, is going to break this piece of code, and it's going to happen at the most inconvenient time, under time pressure and stress. With tests in place you’ll get instant feedback on what broke instead of debugging for hours. It's good for your health.
* When you change something later ‫-‬ the definition of a function, a type, or an object hierarchy, the test will guide you to the required changes to make the rest of the code compatible with that change. Lean on the tests.
  * Example: Changing a response object returned by an API.
* Writing tests will help you find bugs and design flaws faster.
  * If you only test the entire change after completing coding it, and it won't work (you know it rarely works the first time), you will need to spend time finding the exact location of the issue, while requiring you to debug through whole parts of the system. Tests will allow you to contain each issue you are tackling along the way.
* When the change requires modification of multiple functions or classes, testing each unit separately gives you confidence that you are really done with one part of the change, so can move on to the next one. Instead of dealing with multiple pieces of functionality, and therefore multiple potential issues, at once.
* Tests provide faster feedback loops than full system tests. Especially when these contain manual steps.
* Writing a test makes you think more deliberately about design, about inputs and outputs, and in general require you pay more attention to detail. You will get a better overall picture of the change, so you can implement it better.
  * This is mostly beneficial with TDD.
* If you come back to a task that has tests in place, these will quickly give you a good idea of where you stopped.
  * The smaller the unit tests, the greater this benefit.
  * Creating empty failing tests with good names will further help.

## When not to write tests

* The code is likely to be thrown away.