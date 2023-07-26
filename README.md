# ndc-hub

This repository provides a Rust crate to aid development of [Hasura Native Data Connectors](https://hasura.github.io/ndc-spec/). Developers can implement a trait, and derive an executable which can be used to run a connector which is compatible with the specification.

In addition, this library adopts certain conventions which are not covered by the current specification:

- Connector configuration
- State management
- Trace collection

## 🚨 Alpha Warning 🚨

This is currently alpha-quality software, and subject to breaking changes. It is shared here to provide an early preview of what can be expected for connector development in future, and feedback is welcome! If you have any comments, please create an issue.

## Getting started

```sh
cargo build
```

## Run the example connector

```sh
cargo run --bin ndc_hub_example -- \
  --configuration <(echo 'null')
```

Inspect the resulting (empty) schema:

```sh
curl http://localhost:8100/schema
```

(the default port 8100 can be changed using `--port`)
