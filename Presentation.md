---
marp: true
---

# Testing for developers

### Niklas Lundberg
---

Automation

Function testing

Does it fulfill the expectations?
Checks are binary it passes or fails
Can only prove presence of bugs, not absence or correctness
---

# Other types of testing

* Explorary testing
* Performance testing
* Load testing
* System testing

---

# Characteristics

* Isolated (No dependency on unreliable parts)
* Fast (milliseconds)
* Simple (short, doing one thing)
* Good name (clear purpose)
* Independent (run in any order, standalone or in a suite)
---

# Test runners

* NCrunch
* ReSharper
* Test Explorer
* Coderush
* Rider
* CLI

---

# Coverage

Used as metric (Goals, thresholds)
Used as feedback

Execution coverage does not imply all possible combinations have been covered

---

# Test frameworks

## Closed structure
* Machine.Specifications

## Open structure

* xunit
* nunit
* mstest/vstest

---

# A developer tool

## Feedback
* Write just enough code to solve the problem
* Short feedback loop time
* Safety net for regressions
* Guide for better design

---

# Production code first, test(s) after
* [N] Write just enough code to solve the problem
* [N] Short feedback loop time
* [Y] Safety net for regressions
* [N] Guide for better design

---

# Test Driven Development, TDD

* [Y] Write just enough code to solve the problem
* [Y] Short feedback loop time
* [Y] Safety net for regressions
* [Y] Guide for better design

---

# Harder to test
* Statics, singleton, global variables, DateTime.Now/Utc
* Network
* File system
* Concurrency

---

Overcome things that are hard to test

# Statics

* Run checks in serial
* Reset global state in clean-up
* Introduce scope
* Singleton within scope
* Wrap built-in statics (DateTime.Now/NowUtc)

---

# Easy to check

* Pure functions, no side effects, input => output