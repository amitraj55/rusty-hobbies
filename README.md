# rusty-hobbies

A collection of small Rust hobby projects and coding exercises, organized as a single Cargo workspace. Each exercise lives in its own crate so it can be built and run independently.

## Project structure

```
rusty-hobbies/
├── Cargo.toml        # Workspace manifest (resolver = "2")
├── LICENSE           # Apache License 2.0
├── README.md
└── two_sum/          # Exercise: Two Sum
    ├── Cargo.toml
    └── src/
        └── main.rs
```

## Crates

| Crate     | Type   | Description                                              |
|-----------|--------|----------------------------------------------------------|
| `two_sum` | binary | The classic Two Sum problem (currently a starter stub).  |

## Prerequisites

- Rust toolchain **1.85 or newer** (crates use the 2024 edition). Install via [rustup](https://rustup.rs/).

## Usage

From the workspace root:

```sh
# Build every crate in the workspace
cargo build

# Run a specific crate
cargo run -p two_sum

# Run tests for all crates
cargo test
```

## Adding a new exercise

1. Create a new crate inside the workspace:
   ```sh
   cargo new <exercise_name>
   ```
2. Add it to the `members` list in the root `Cargo.toml`:
   ```toml
   [workspace]
   resolver = "2"
   members = ["two_sum", "<exercise_name>"]
   ```
3. Run it with `cargo run -p <exercise_name>`.

## License

This project is licensed under the Apache License 2.0 — see [LICENSE](LICENSE) for details.
