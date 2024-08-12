# sccache-setup-action

A github action to install and setup sccache to speed up your builds

It installs (on Windows and MacOS), recover a cached sccache cache using the cache action
and setup and run a sccache server.

On Linux, it assumes sccache is available.

```
  - name: Install and setup sccache
    uses: f3d-app/sccache-setup-action@v1
    with:
      key: MyKey-0
```

Resulting caches can be seen in your actions tab.
