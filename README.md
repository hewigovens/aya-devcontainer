# [Devcontainer](https://containers.dev/) for [Aya-rs](https://github.com/aya-rs/aya)

Aya is an eBPF library for Rust, from `Environment` section on [aya-rs/book](https://aya-rs.dev/book/start/development/), `bpf-linker` only works on `linux x86_64 system`

To simplify the development environment setup, we can use [Devcontainer](https://containers.dev/) to build and run eBPF program in Rust.

for more details, please take a look at `devcontainer.json` and `Dockerfile`.

```bash
.
├── .devcontainer
│   ├── devcontainer.json
│   └── Dockerfile
```

## How to Use

- Open this repository in VSCode
- Install [Dev Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) extension
- Open the command palette (Shift+Command+P)
- Select `Dev Containers: Reopen in Container`

Generate ebpf app from [aya-template](https://github.com/aya-rs/aya-template)

```bash
cargo generate https://github.com/aya-rs/aya-template

cd <your_app_path>

# build both ebpf and userspace app
cargo xtask build
```

## Credits

Tweaked from Kevin Sookocheff's [blog post](https://sookocheff.com/post/kubernetes/developing-an-aya-rs-app-using-devcontainers/).
