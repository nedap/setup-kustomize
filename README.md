
This action sets up kustomize for use in actions by:

- Downloading a pinned version of `kustomize` from its GitHub release and adding it to `$PATH`

The version defaults to a pinned release. Nothing is resolved at run time: the
action does not fetch the upstream installer script and does not call the GitHub
API to look up the latest release.

```yaml
steps:
  - uses: nedap/setup-kustomize@v1
  - run: kustomize version
```

```yaml
steps:
  - uses: nedap/setup-kustomize@v1
    with:
      kustomize-version: 5.0.1
  - run: kustomize version
```
