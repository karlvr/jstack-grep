# Jstack Grep

The `jstack` tool outputs stack traces from Java programs. `jstack-grep` helps to search through those stack traces.

## Usage

```shell
jstack-grep [-f] [-i <pattern>] [-n] <pattern> [-o <pattern>] [-a <pattern>] [-x <pattern>] <pid | - | filename | process name>
```

|Option|Description|
|------|-----------|
|`-f`|Show full stacktraces.|
|`-i <pattern>`|Only show stacktrace lines matching pattern. Can be specified multiple times.|
|`-n`|Turn off case-insensitive pattern matching.|
|`-o <pattern>`|Additional patterns that MAY match. Can be specified multiple times.|
|`-a <pattern>`|Additional patterns that MUST match. Can be specified multiple times.|
|`-x <pattern>`|Additional patterns that MUST NOT match. Can be specified multiple times.|

If no `-i` options are specified, only lines matching the search `<pattern>` or any `-o` and `-a` patterns are shown.

Matching is case-insensitive by default.
