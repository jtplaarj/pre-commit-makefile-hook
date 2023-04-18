<!--
 Copyright (c) 2023 Jesús Lázaro
 
 This software is released under the MIT License.
 https://opensource.org/licenses/MIT
-->
![GitHub](https://img.shields.io/github/license/jtplaarj/pre-commit-makefile-hook)
---
title: pre-commit make action
author: Jesús Lázaro
date: 2023-04-18
license: MIT
---

This pre-commit hook executes a Makefile target. It is useful to run tests, linters, etc.

## Usage

Add this to your `.pre-commit-config.yaml`:

```yaml
-   repo: https://github.com/jtplaarj/pre-commit-makefile-hook.git
    rev: V1.0.0
    hooks:
    -   id: make
    # -   args: [test]
```

## Hooks available

### `make`

Executes a Makefile target. You can pass the targets to execute as arguments. By default, it executes the `pre-commit-hook` target.

A sample Makefile could be:

```makefile
pre-commit-hook: update-readme
```

Which is my main usage, so that the README.md is updated before committing.

## License

This library is free software; you can redistribute it and/or modify it under the terms of the MIT license. See [LICENSE](LICENSE) for details.
