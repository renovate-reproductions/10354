# renovate-bug-10268-reproduce

A minimal reproduction of issue https://github.com/renovatebot/renovate/issues/10268.

The `setup.cfg` file contains tilde ranges, in order to stick to minor updates in some repos.
Renovate identifies these, but when it opens a PR, it narrows the range by adding a patch version.
