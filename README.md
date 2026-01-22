## 安装 Rust
```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

## VSCode Plugin


## 安装 Cargo generate
cargo generate 是一个用于生成项目模板的工具。它可以基于现有的 Github repo 作为模板来初始化一个新的项目。
```bash
cargo install cargo-generate
```
基于模板仓库初始化项目
```bash
cargo generate zlx2019/rust-genesis
```

## Install pre-commit
```bash
pip install pre-commit
```

## Install cargo-deny
用于检查依赖库版本的安全性。
```bash
cargo install --locked cargo-deny
```

## Install typos
typos 是一个拼写检查工具。
```bash
cargo install typos-cli
```

## Install git-cliff
用于生成 Changelog 的工具。
```bash
cargo install git-cliff
```

## Install nextest
Rust 增强版单测工具。
```bash
cargo install cargo-nextest --locked
```
