---
description: "Optimize naming for grep/ack-based code search"
alwaysApply: true
---

# EzGrep Rules (Search-First Naming)

EzGrep is a language-agnostic naming rule: choose names in your repo with grep-style search in mind.

Optimize for simple, reliable text searches over conventional naming aesthetics. If a name is easy to `grep`/`ack` uniquely and consistently, it’s a good EzGrep name.

Key principle: **repeat the exact token you want to search for**.

## Guidelines

- Prefer names that are distinctive and stable across the codebase.
- When referencing a definitional unit (class/function/type), repeat its exact name in related identifiers.
- It is acceptable to mix casing or break stylistic conventions if it improves searchability.
- Avoid “smart” abbreviations that make search terms ambiguous.

## Example (Python)

If you have a class named `HelperDaemon` and a function that prints those objects:

Allowed (search-first):

```py
class HelperDaemon:
    ...

def print_HelperDaemon(obj: HelperDaemon) -> None:
    ...
```

Not preferred (convention-first, harder to search precisely):

```py
class HelperDaemon:
    ...

def print_helper_daemon(obj: HelperDaemon) -> None:
    ...
```

With EzGrep, searching for `HelperDaemon` finds the class, its usage sites, and related helpers without needing multiple search patterns.

## Tools

This rule is designed for fast text search tools like `grep` and `ack`:

- https://beyondgrep.com (ack)
