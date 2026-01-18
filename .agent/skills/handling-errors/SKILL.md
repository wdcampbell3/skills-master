---
name: handling-errors
description: Provides patterns and best practices for resilient error handling and debugging. Use when implementing error handling, designing error-resilient APIs, or troubleshooting production issues.
---

# Error Handling & Troubleshooting Patterns

## When to use this skill
- Implementing error handling in new features.
- Designing error-resilient APIs.
- Debugging and troubleshooting production issues.
- Improving application reliability.
- Implementing retry and circuit breaker patterns.
- Handling async/concurrent errors.

## Core Concepts

### 1. Error Handling Philosophies
- **Exceptions**: Traditional try-catch, disrupts control flow. (Python, Java, TS)
- **Result Types**: Explicit success/failure, functional approach. (Rust, Go, TS)
- **Option/Maybe Types**: For nullable values.

**When to Use Each:**
- **Exceptions**: Unexpected errors, exceptional conditions.
- **Result Types**: Expected errors, validation failures.
- **Panics/Crashes**: Unrecoverable errors, programming bugs.

### 2. Error Categories
- **Recoverable Errors**: Network timeouts, missing files, invalid user input.
- **Unrecoverable Errors**: Out of memory, stack overflow, programming bugs.

## Best Practices
1.  **Fail Fast**: Validate input early, fail quickly.
2.  **Preserve Context**: Include stack traces, metadata, and timestamps.
3.  **Meaningful Messages**: Explain what happened and how to fix it.
4.  **Log Appropriately**: Error = log; expected failure = don't spam logs.
5.  **Handle at Right Level**: Catch where you can meaningfully handle.
6.  **Clean Up Resources**: Use try-finally, context managers, `defer`.
7.  **Don't Swallow Errors**: Log or re-throw, don't silently ignore.

## Common Pitfalls
- **Catching Too Broadly**: `except Exception` hides bugs.
- **Empty Catch Blocks**: Silently swallowing errors.
- **Logging and Re-throwing**: Creates duplicate log entries.
- **Not Cleaning Up**: Forgetting to close files/connections.
- **Poor Error Messages**: "Error occurred" is not helpful.

## Resources
Explore specific implementing patterns for your language or use case:

- **Python Patterns**: 👉 [`resources/python-patterns.md`](resources/python-patterns.md)
  (Custom Exceptions, Content Managers, Retry Decorators)

- **TypeScript/JS Patterns**: 👉 [`resources/typescript-patterns.md`](resources/typescript-patterns.md)
  (Custom Errors, Result Types, Async Handling)

- **Rust Patterns**: 👉 [`resources/rust-patterns.md`](resources/rust-patterns.md)
  (Result, Option, Custom Error Types)

- **Go Patterns**: 👉 [`resources/go-patterns.md`](resources/go-patterns.md)
  (Explicit Returns, Sentinel Errors, Wrapping)

- **Universal Patterns**: 👉 [`resources/universal-patterns.md`](resources/universal-patterns.md)
  (Circuit Breaker, Error Aggregation, Graceful Degradation)
