# CONTRIBUTING
If you're interested in contributing to `super_embed`, please adhere to the following guidelines.

## Project principles
* Aggressive composition: Build small, effective tools that are designed to work with other small tools to achieve broader functionality.
* Establish strong encapsulation boundaries: Keep unrelated concepts completely independent (including transitive dependencies).
* If you can't see it, it doesn't exist: Every feature should have a runnable demo.
* Tests are not optional: Every feature must be tested, and those tests must run in CI.

**A few specifics**

* Classes and behaviors that are required for `super_embed` but are not specific to the project goals should be placed within the `infrastructure` package.
* Meaningless names like "manager", "helper", "utility", "data", "model" will not be accepted unless there is a strong contextual reason to do so.
* If the term "controller" is used, it must specifically refer to the Flutter concept of a controller.
* `super_embed` is a Dart-only solution. Do not contribute platform code.

## Bug tickets must include reproduction steps
Every development machine, environment, and project configuration is unique. It can be difficult or impossible to reproduce bugs without appropriate guidance from the person who found the bug.

If you file a bug, you must include **minimal reproduction steps** so that project maintainers can reproduce the bug. A "minimal" set of reproduction steps is a set of steps that include details that are needed to reproduce the bug and nothing more.

Bug tickets that lack minimal reproduction steps will be closed.

## Feature requests must include the motivation
Developers often see a problem and then immediately jump to a solution. But jumping to a solution prevents project maintainers from considering the broader context of a given problem.

All feature request tickets must be framed in terms of a motivation, rather than a specific change to the project.

## Pull requests must include effective tests
Every change to the project must include effective tests.

An effective test meets the following criteria:

 * Uses the lowest level test tools that accomplish the testing goals.
   * Dart language tests for non-UI behaviors. Unit tests, when feasible.
   * Widget tests for user interactions.
   * Golden tests for visual goals.
   * Integration tests as a last resort. They take much longer to run and they depend on specific platforms.
 * Doesn't test things that are already tested (avoid useless redundancy).
 * Does test all edge cases.
 * Is grouped appropriately.
 * Is named appropriately.
 * Is readable and comprehensible by project maintainers.