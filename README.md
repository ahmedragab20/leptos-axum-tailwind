# Axum-Leptos Full-Stack Application

A modern, full-stack web application template combining the power of Rust's ecosystem for both frontend and backend development.

_the template is based on the [Axum-Leptos template](https://github.com/leptos-rs/leptos/tree/main/examples/tailwind_axum)_

## Tech Stack

- **Frontend**:
  - [Leptos](https://leptos.dev/) - A modern Rust web framework for building reactive web applications
  - [TailwindCSS](https://tailwindcss.com/) - A utility-first CSS framework for rapid UI development
  - WebAssembly - For running Rust code in the browser

- **Backend**:
  - [Axum](https://github.com/tokio-rs/axum) - A ergonomic and modular web framework built with Tokio
  - [Tokio](https://tokio.rs/) - Asynchronous runtime for Rust
  - [cargo-leptos](https://github.com/leptos-rs/cargo-leptos) - Build tool for Leptos applications

- **Testing**:
  - [Playwright](https://playwright.dev/) - End-to-end testing framework

## Getting Started

### Prerequisites

1. Install Rust (nightly):
```bash
rustup toolchain install nightly --allow-downgrade
rustup target add wasm32-unknown-unknown
```

2. Install cargo-leptos:
```bash
cargo install cargo-leptos --locked
```

3. Install Node.js dependencies:
```bash
npm install
cd end2end && npm install
```

### Development

1. Start the development server:
```bash
cargo leptos watch
```
This will start your application at `127.0.0.1:3000`

2. For production build:
```bash
cargo leptos build --release
```

### Testing

Run end-to-end tests:
```bash
cargo leptos end-to-end
```

## Project Structure

- `src/`
  - `main.rs` - Server entry point
  - `lib.rs` - Shared code between client and server
  - `app.rs` - Main application component
- `style/` - CSS and TailwindCSS files
- `end2end/` - End-to-end tests
- `Cargo.toml` - Rust dependencies
- `package.json` - Node.js dependencies

## License

This project is released under the Unlicense. Feel free to use it as a starting point for your own applications.
