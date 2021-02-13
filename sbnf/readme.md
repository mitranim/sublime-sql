Experimental implementation of the Postgres SQL dialect in [SBNF](https://github.com/BenjaminSchaaf/sbnf). Very incomplete. Blocked by the following issues:

* At the time of writing (for the current versions of ST4 and SBNF), using the generated syntax causes ST to hang in some scenarios.

* Lack of imports/inheritance in SBNF makes it harder to reuse common parts between related syntaxes.
