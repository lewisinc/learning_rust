# Learning Rust
I want to learn Rust, let's do it the "Right Way"

## Rust's tools
There are a few different tools, both official and community controlled that I feel it'll be important to keep an eye on and play around with. I'll try to list some of the, subjectively, most important...

### [Rustup](https://rustup.rs)
Installed with `curl https://sh.rustup.rs -sSf | sh`, Rustup is a toolchain manager allowing you to do several things. Among those is add new architecture targets to compile for.

See all the available targets you can build for with `rustup target list`.

Rustup also works similarly to rbenv in the sense that you can switch between different build environments by altering your `rustup toolchain` and switching between Rust's Stable, Nightly, and Beta channels. Beyond this essential functionality you'll have to learn for yourself.

### [Cargo](https://crates.io)
Analogous to NPM or RubyGems. Cargo - along with its counterpart Crates.io - is a build system and dependency manager that allows you to create an empty project template and populate it with metadata about your project as well as define versioned dependecies that your 'crate' uses.

Cargo is fairly easy to get started in with documentation a `--help` away.

#### Examples of Cargo usage
`cargo new $PROJECT_NAME` initializes an empty project. Newly initialized projects have nice 'Hello World.' print statement in `$PROJECT/src/main.rs` to help get you started. The `--bin` flag tells cargo your project is a standalone application. By default cargo assumes you are writing a library with which you'll embed in another project. I can only assume this decision was made to highlight the idea that you don't need to commit fully to using Rust, and can instead replace functionality in an existing proejct piece-by-piece in the same way you might optimize a project by replacing function implementations in a more performant language such as C or C++.

`cargo run` builds and runs your project. Some projects will include examples in their repositories. These can usually be run with `cargo run --example $EXAMPLE_NAME`.

`cargo test` will run any tests you write for your project

`cargo build` will build your project. Various flags are included, such as the ability to build a `--release` build, or build for a specific architecture target (currently targets are limited to those supported by the LLVM project).

### [Rust Language Server](https://github.com/jonathandturner/rls)
While not really relevant right now, in the "near" future this will allow automatic linting, error checking, refactoring among other cool/useful things to any IDE that implements the right functions. In theory this means that your IDE relies on the Rust compiler and a crate `racer` to do all the heavy lifting for source code editing, meaning you'll - in theory - get an identical experience regardless of which IDE you use. Maybe not super relevant yet, but it will be.

### [Tokio.rs](https://tokio.rs)
A networking platform that's main use is for implementing asynchronous networking protocols. I'm not much of a networking protocol guy, but it seems to be a pretty cool project.

### [Neon](https://www.neon-bindings.com)
Rust bindings for Node.JS, allowing you take advantage of Rust's speed and parallelism to do some really cool shit.

``` bash
# Install Rust.
$ curl https://sh.rustup.rs -sSf | sh

# Install the Neon CLI.
$ npm install --global neon-cli

# Create a new project!
$ neon new my-project
```

### [RuRu](https://github.com/d-unseductable/ruru)
Like Neon, except now Rust can interop with Ruby. Woah.
