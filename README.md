# setup-stubcc

A GitHub Action for downloading and installing [mario-campos/stubcc](https://github.com/mario-campos/stubcc)!

```yaml
- name: Setup stubcc
  uses: mario-campos/setup-stubcc@main
  id: setup-stubcc
- name: Stub C Compilation
  run: $CC foo.c
  env:
    CC: ${{ steps.setup-stubcc.outputs.gcc }}
```
