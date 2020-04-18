# Backlinks

`Backlink` is a utility to summarise links between files.

If we consider three files `A`, `B`, and `C`.

- No file links to `C`
- `A` contains a link to `B`

Under this condition,

- `A` is a backlink of `B` (B is pointed-to by A)
- `B` is a forward link of `A` (A points to B)
- `C` is an orphan (no other file links to it)

## Usage

```
backlinks [-foc] FILES...

-f --forward   Show forward links from each file instead of backlinks
-o --orphan    Show orphaned links
-c --count     Show count link type for each file
```

`-f` and `-c` can be combined.

If `FILES...` is given, then will only shop backlinks or forward links for those files. Otherwise, all `.md` files under the current directory will be used.
