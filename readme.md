## Overview

Sublime Text syntax definitions for SQL, rebuilt from scratch. Currently only the Postgres dialect is implemented.

Differences from the built-in SQL syntax and the PgSQL package available on Package Control:

* Detects keywords contextually. Only _reserved_ keywords are context-free. Other keywords are detected only where they're expected.
* Detects types contextually, where types are expected, without relying on a whitelist of built-ins. There's no difference between pre-defined and user-defined types.
* No unnecessary scopes for built-in functions or types.
* Prefers to scope keywords as `keyword` rather than `storage` (may reconsider for some contexts).
* Adheres more closely to ST scope conventions while respecting SQL semantics.
* Supports ordinal parameters like `$1` and named parameters like `:ident`.

Current limitations:

* Only the Postgres dialect is implemented.
* Doesn't implement some contextual keywords such as `on update cascade`.
* NYI: PL/PGSQL.
* NYI: multi-word types.
* NYI: function calls.
* ... Probably a few more NYI.

Despite the limitations, I consider this much more usable than the previously-mentioned packages.

## Installation

Clone the repo and symlink it to your Sublime packages directory. Example for MacOS:

```sh
git clone https://github.com/mitranim/sublime-sql.git
cd sublime-sql
ln -sf "$(pwd)" "$HOME/Library/Application Support/Sublime Text 3/Packages/"
```

To find the packages directory on your system, use Sublime Text menu → Preferences → Browse Packages.

## License

https://unlicense.org

## Misc

I'm receptive to suggestions. If this package _almost_ satisfies you but needs changes, open an issue or chat me up. Contacts: https://mitranim.com/#contacts