* Import using `use`. eg) `use std::io;`.

* Rust has a global scoped crates, which are defined in `std::prelude::v1`. If not included in `prelude` must be imported.
`std::io` is not in prelude.

* `use std::io` makes available `io` type as a local(to importing file) variable. Saves us from writing
`std::io::SOME_ASSOCIATE_FUNCTION`

* Variables are created with `let` statement. 

* Variables are immutable by default.

* Use `mut` before variable name to make it mutable.

* Create UTF-8 String instance with `String::new();`.

* `String::new` read as *associate function of `String` type*. associate function is similar to static method.

* `std::io::stdin()` returns an *instance* of `std::io::Stdin`, a type representing input from terminal.

* `std::id::stdin().read_line()` is a *method* of `std::io::Stdin` instance, that passes input(buffer) from terminal as
a string to passed in *mutable* argument.

* `&` indicates it's a reference. Pass by reference is done this way. references are immutable as well.

* `&guess` is an immutable reference. `&mut guess` is a mutable reference. 04_ for more detail.

* `read_line` method returns `io::Result` type, which is a monad (`Either` monad with `Err` or `Ok`).

* `io::Result` type has `expect` method which is similar to `getOrThrow` with passed in message.
eg) `expect('Failed to read line')` will throw error with `"Failed to read line"` message if `Err` type is returned.

* If returned type of `.read_line` method is `Ok` type `.expect` method will unwrap value contained in `Ok` and return it.

* Placeholder in string is expressed with `{}`. eg) `println!("x = {} and y = {}", x, y)`

* `binary crate` only contains executable. `library crate` has source code.

* `crates.io` is like a `npmjs.com`

* `Cargo.lock` is like `package-lock.json`

* `cargo update` is like `npm update`, uses semver. Updates PATCH version not MINOR or MAJOR version.
If MINOR or MAJOR version update is needed then change `Cargo.toml` with specific MAJOR or MINOR version.
Note: `cargo update` updates `Cargo.lock` only and not `Cargo.toml`. <Q::--save flag?>

* Traits, unlike `use std::io` where `io` is associate function, `use rand::Rng` (notice Capital R of `Rng`) is a trait.
Trait defines methods that `rand` implements. More on traits in 10_.

* TODO: rand::thread_rng