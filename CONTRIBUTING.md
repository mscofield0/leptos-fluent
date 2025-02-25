# Contributing

## Setup

```bash
python3 -m pip install pre-commit
pre-commit install
```

## Tests

[!NOTE] End to end tests are located at _end2end/_.

### End to end tests

You need to install a browser and run:

```bash
cd tests
wasm-pack test --{browser} --headless
```

Where `{browser}` is one of `firefox`, `chrome`, or `safari`. For example:

```sh
cd end2end
wasm-pack test --firefox --headless
```

If you want to run a test suite pass it in the `--test` flag.
For example, to run the `csr_complete` test suite run:

```sh
cd end2end
wasm-pack test --firefox --headless --test csr_complete
```

### Unit tests

```sh
cargo test -p leptos-fluent -p leptos-fluent-macros
```

## Documentation

```sh
cargo doc --open --no-deps
```
