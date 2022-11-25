---
marp: true
---

# Testing for developers

### Niklas Lundberg
---

# Functional testing

* Does it fulfill the expectations?
* Checks are binary, it passes or fails
* Can only prove presence of bugs, not absence nor correctness of code
* Automation

---

# Other types of testing

* Explorary testing
* Scripted, manual testing
* Performance testing
* Load testing
* System testing

---

# Testing as a developer tool

## Feedback
* Write just enough code to solve the problem
* Short feedback loop time
* Safety net for regressions
* Guide for better design

---

# Production code first, tests after
* [N] Write just enough code to solve the problem
* [N] Short feedback loop time
* [Y] Safety net for regressions
* [N] Guide for better design

---

# Test Driven Development, TDD, tests first

* [Y] Write just enough code to solve the problem
* [Y] Short feedback loop time
* [Y] Safety net for regressions
* [Y] Guide for better design

---

# Characteristics of good tests

* Isolated (No dependency on unreliable parts)
* Fast (milliseconds)
* Simple (short, doing one thing)
* Good name (clear purpose)
* Independent (run in any order, standalone or in a suite)
* Run in parallell

---

# Code coverage

* Used as metric (Goals, thresholds)
* Used as feedback
* Execution coverage does not imply all possible combinations have been covered

---

# Easy to test

* Pure functions, no side effects, input => output

# Harder to test
* Statics, singletons, global variables, DateTime.Now/Utc
* Network
* File system
* Concurrency

---

# Overcome things that are hard to test

## Statics

* Run checks in serial
* Reset global state in clean-up
* Introduce scope
* Singleton within scope
* Wrap built-in statics (DateTime.Now/NowUtc)
* Abstractions

---

# Test balance

* Inside-out
* Outside-in
* Refactoring
* Over-abstracting
* Dependencies

---

# Test runners

* NCrunch
* ReSharper
* Test Explorer
* CodeRush
* Rider
* CLI

---

# Test frameworks

## Closed structure
* Machine.Specifications

## Open structure

* xunit
* nunit
* mstest/vstest

---

# Structuring tests

* Given/When/Then Arrange/Act/Assert
* Naming
* Multiple assertions
* Categories (fast, slow, dependencies)
* Fluent assertions

---

# What to test

* Happy path
* Function return values
* State changes, side effects
* Boundary values (off-by-one)
* Input
* Error handling

---

# Future topics

* Testing legacy code in practice
* Testing in production
    * Overrides
    * What-if