# rust-mart-tutorial
Example of single page application with Rust http://www.sheshbabu.com/posts/rust-wasm-yew-single-page-application/


## Random notes

#### 1. $ cargo new --lib rust-mart-tutorial
To start a new package with Cargo, use cargo new: `$ cargo new hello_world --bin`

We’re passing `--bin` because we’re making a binary program: if we were making a library, we’d pass `--lib`. This also initializes a new git repository by default. If you don't want it to do that, pass `--vcs none`.

More info: https://doc.rust-lang.org/cargo/guide/creating-a-new-project.html

#### 2. Yew UI
Yew is a modern Rust framework for creating multi-threaded front-end web apps with WebAssembly.

- **component-based framework** which makes it easy to create interactive UIs (especially for Developers who have experience with frameworks like React and Elm).
- **great performance** by minimizing DOM API calls and by helping developers easily offload processing to the background using web workers.
- **javaScript interoperability**, allowing developers to leverage NPM packages and integrate with existing JavaScript applications.

More info: https://yew.rs/docs/en/intro/


#### 3. Build and Run/Serve
`$ cargo make build`
Start the build process which stay in listening mode and automatically builds the project when a new change is made.

`$ cargo make serve`
It can be run in parallel (new terminal). The result will be available at http://localhost:3000 .

## Troubleshooting

#### 1. Failed to run custom build command for opensll-sys

It can happen during the setup

Follow: https://github.com/sfackler/rust-openssl/issues/1021

`sudo apt install pkg-config`

Ubuntu: `sudo apt install libssl-dev`

Fedora: `sudo apt install openssl-devel`