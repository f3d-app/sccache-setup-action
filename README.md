# sccache-setup-action

A github action to install and setup sccache to speed up your builds

It installs (on Windows using `choco` and on MacOS using `brew`), recover a cached sccache cache using the github cache action
then setup and run a sccache server.

On Linux, it assumes sccache is available.

Example usage:

```
  - name: Install and setup sccache
    uses: f3d-app/sccache-setup-action@v1
    with:
      key: MyKey-0
```

Resulting caches can be seen in your actions tab.

To check the sccache action is behaving as expected, it is possible to add the following at the end of your job:

```
  - name: Stop and check sccache
    shell: bash
    run: sccache --show-stats
```
