# renovate-bug-10268-reproduce

A minimal reproduction of issue https://github.com/renovatebot/renovate/issues/10268.

The `setup.cfg` file contains tilde ranges, in order to stick to minor updates in some repos.
Renovate identifies these, but when it opens a PR, it narrows the range by adding a patch version.

For example, in this repository we're using `click~=7.1`, so an expected Renovate PR would change it
to `click~=8.0`.

Right now, both PRs opened by Renovate narrow the range (to 7.1.2 and 8.0.1 respectively):
- https://github.com/ofir123/renovate-bug-10268-reproduce/pull/2
