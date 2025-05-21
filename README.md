# RustyAct

[![Crates.io](https://img.shields.io/crates/v/rustyact)](https://crates.io/crates/rustyact) [![Docs.rs](https://docs.rs/rustyact/badge.svg)](https://docs.rs/rustyact) [![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

RustyAct is a fast, extensible project scaffolding tool inspired by Create React App, but built in Rust for maximum performance and safety. Generate modern web applications (JS & TS), PWAs, SSR projects, and more with zero-config or fully interactive setups.

---

## 🚀 Features

* **Blazing Fast**: Written in Rust, leveraging async I/O and minimal filesystem syncs
* **Zero-Config Init**: `rustyact init <project-name>` to scaffold with sensible defaults
* **Interactive Mode**: Customize templates, styles, state management, testing frameworks
* **Multiple Templates**:

    * JavaScript (ESM/CJS) & TypeScript
    * PWA, SSR, Mobile (React Native)
    * Custom community templates via plugin marketplace
* **Plugin System**: Add or write plugins for i18n, GraphQL, CMS, UI kits
* **Dev Server**: Hot reload, file watching, proxy support & custom middleware
* **Build & Publish**: One command bundle & optimize your output
* **Config Migration**: Upgrade templates and project configs seamlessly
* **Rich CLI UX**: Colored output, progress bars, prompts, and error reporting
* **Cross-Platform**: Windows, macOS, Linux support

---

## 🛠️ Installation

Ensure you have [Rust & Cargo](https://www.rust-lang.org/tools/install) installed.

```bash
cargo install rustyact
```

Or add to your project:

```toml
[dependencies]
rustyact = "^0.1.0"
```

---

## 🎬 Quick Start

```bash
# Scaffold a new project
rustyact init my-app

# Change directory
cd my-app

# Start development server
rustyact serve

# Build for production
ttyrustyact build
```

---

## ⚙️ CLI Commands

| Command                      | Description                                             |
| ---------------------------- | ------------------------------------------------------- |
| `rustyact init <name>`       | Scaffold a new project with default or interactive mode |
| `rustyact serve [options]`   | Run dev server with hot reload                          |
| `rustyact build [options]`   | Bundle and optimize for production                      |
| `rustyact test`              | Run unit & E2E tests                                    |
| `rustyact plugin add <name>` | Install community or custom plugin                      |
| `rustyact config`            | View or edit global/project configuration               |

Use `rustyact <command> --help` for detailed flags and options.

---

## 🔌 Plugin System

RustyAct supports dynamic plugins shipped as Cargo crates or binaries:

1. **Add a plugin** via CLI:

   ```bash
   rustyact plugin add rustyact-plugin-i18n
   ```
2. **List installed plugins**:

   ```bash
   rustyact plugin list
   ```
3. **Develop your own plugin**:

    * Implement the RustyAct plugin trait
    * Publish to crates.io
    * Users can install via CLI

---

## 🗂️ Template Packs

Templates live in separate repos or archives. Use remote or local packs:

```bash
# Use an official remote pack
ttyrustyact init my-pwa --template https://github.com/rustyact/pwa-template

# Use a local folder
ttyrustyact init custom-app --template ./my-local-template
```

---

## 🛡️ Configuration

RustyAct reads from `rustyact.config.toml` in project root and `$HOME/.config/rustyact/config.toml`:

```toml
# Example project config
project_name = "my-app"
default_template = "typescript"

[features]
state = "zustand"
testing = "jest"
```

---

## 🛣️ Roadmap

* [ ] Template Marketplace
* [ ] Official CI/CD integrations
* [ ] Dockerized builds
* [ ] Improved plugin SDK & docs
* [ ] UI for interactive templates

Contributions and feedback are welcome!

---

## 🙌 Contributing

1. Fork the repo
2. Create a feature branch (`git checkout -b feat/awesome`)
3. Commit your changes (`git commit -m "feat: add awesome feature"`)
4. Push to the branch (`git push origin feat/awesome`)
5. Open a Pull Request

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details.

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

Made with ❤️ and 🚀 by the RustyAct team
