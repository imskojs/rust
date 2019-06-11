* Scaffold with `cargo new helloCargo`.

* New cargo cannot start with numeric letter.

* `Cargo.toml` is like `package.json`

* Packages or modules are called `crates`.

* To make a project that did not use cargo into cargo project simply make `Cargo.toml` and `src/` folder.

* Rust recommends snake_case. `[package].name` must be snake_case, if not Rust force converts. 

* Build with `cargo build` in project root.

* Run with `./target/debug/hello_cargo`.

* Build and Run with one command `cargo run` in project root.

* Only re-compiles if there is a change in source code.

* Check whether source is compilable with `cargo check`.

* For production code run `cargo build --release`, it produces optimized code in `target/release`.
Similar to `ng build --prod`

* `target/debug` for development, `target/release` for production.
