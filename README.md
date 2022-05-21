# setup-stubcc

A GitHub Action for downloading and installing [mario-campos/stubcc](https://github.com/mario-campos/stubcc)! The only requirement is that the runner is x86_64 Linux.

```yaml
jobs:
  runs-on: ubuntu-latest # required
  steps:
  - name: Setup stubcc
    uses: mario-campos/setup-stubcc@v1
    id: setup-stubcc
  - name: Stub C Compilation
    run: $CC foo.c
    env:
      CC: ${{ steps.setup-stubcc.outputs.gcc }}
```
