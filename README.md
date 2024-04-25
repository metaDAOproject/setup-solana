# Setup Solana

An optimized action for installing the [Solana Tool Suite](https://docs.solana.com/cli/install-solana-cli-tools).

If you use Anchor, you should also check out [Setup Anchor](https://github.com/metaDAOproject/setup-anchor).

# Usage

Here's an example workflow:

```yaml
name: example-workflow
on: [push]
jobs:
  run-solana:
    runs-on: ubuntu-20.04
    steps:
      - uses: actions/checkout@v3
      - uses: metadaoproject/setup-solana@v1.0
      - run: solana block
        shell: bash
```

This will use the default versions of the Solana Tool Suite, 16.15.1. You can also configure this version like so:

```yaml
steps:
  - uses: actions/checkout@v3
  - uses: metadaoproject/setup-solana@v1.0
    with: 
      solana-cli-version: '1.10.32'
```

# License

The scripts and documentation in this project are released under the [MIT License](LICENSE).
