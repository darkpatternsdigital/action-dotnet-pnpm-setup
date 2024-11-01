
## Usage

```yaml
on:
  - push
  - pull_request

jobs:
  cache-and-install:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout
        uses: actions/checkout@v4
      - uses: darkpatternsdigital/actions/sln-restore@v1
        with:
            node-version: 22
```
