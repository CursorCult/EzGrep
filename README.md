# EzGrep

EzGrep enforces search-first naming. Every name is chosen to be easy to find with fast text search tools like `grep` or `ack`.

**Install**

```sh
pipx install cursorcult
cursorcult link EzGrep
```

Rule file format reference: https://cursor.com/docs/context/rules#rulemd-file-format

**When to use**

- You rely heavily on codebase search to navigate and refactor.
- Your repo has many similar concepts where ambiguous names slow you down.
- You want related helpers to show up with a single search term.

**What it enforces**

- Names are optimized for exact-token search, not purely for style consistency.
- Related identifiers repeat the exact definitional name you’d search for.
- Breaking conventional casing is acceptable when it improves grepability.

**Credits**

- Developed by Will Wieselquist. Anyone can use it.

**Links**

- ack: https://beyondgrep.com

**See also**

- UNO: https://github.com/CursorCult/UNO.git
