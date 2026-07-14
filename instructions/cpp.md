---
applyTo: applyTo: "**/*.{cpp,h,hpp,hxx}"
---

Modern C++ Guidelines
=====================

Overall philosophy
------------------

Build the core as value-oriented, functional-style in C++23 using plain structs, pure functions, and explicit error handling.

**Core Principles**

* Prefer std::expected<T, Error> for recoverable errors. Reserve exceptions for truly exceptional failures.
* Use rich error types (enums or structs), not strings.
* Use std::ranges, std::views, and standard algorithms over manual iterator loops.
* Prefer value semantics and immutable data where practical (const correctness).
* Represent domain data as simple structs.
* Keep algorithms as pure free functions; classes should primarily manage state/resources.
* Use RAII for resource management.
* Use std::optional for 'not found' and std::expected for 'operation failed'.
* Favor templates/concepts over inheritance except where runtime polymorphism is required (e.g. plugin systems).
* Aim for high unit test coverage in the core libraries.

**Standard Library vs External Libraries**

* Prefer the highest standard for C++ development (C++23)
* Use Boost as a defacto standard (i.e. if no clean solution exists in the standard library, or there is a more readable option via Boost, use Boost)


**Preferences**

* 


