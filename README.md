# Uncommon Kotlin Collection Modification Error

This repository demonstrates a subtle but potentially problematic behavior when using the `removeIf` function on mutable collections in Kotlin. The `removeIf` function modifies the collection in-place while iterating, which can lead to unexpected results if not carefully considered.

The `bug.kt` file shows the issue, while `bugSolution.kt` provides a correct approach.

## The Problem

The problem arises from directly modifying a collection while iterating over it using a method like `removeIf`. This can skip elements or cause incorrect removal.  The original code iterates through elements, removes some, which alters indices and causes problems in iteration.