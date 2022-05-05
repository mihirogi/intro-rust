# helloworld
## はじめるために

WSL2上に環境を構築してみる

[公式の導入](https://www.rust-lang.org/ja/tools/install)に従う

```sh
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

インストールの風景を見てると、以下のようなものがダウンロードされてた

```sh
info: downloading component 'cargo'
info: downloading component 'clippy'
info: downloading component 'rust-docs'
info: downloading component 'rust-std'
```

インストールできたこと確認

```sh
~/work/repo/intro-rust on  main 
❯ rustup --version
rustup 1.24.3 (ce5817a94 2021-05-31)
info: This is the version for the rustup toolchain manager, not the rustc compiler.
info: The currently active `rustc` version is `rustc 1.60.0 (7737e0b5c 2022-04-04)`
~/work/repo/intro-rust on  main 
❯ cargo --version
cargo 1.60.0 (d1fd9fe 2022-03-01)
~/work/repo/intro-rust on  main 
❯ rustc --version
rustc 1.60.0 (7737e0b5c 2022-04-04)
```


### cargo

[ビルドシステム兼パッケージマネージャー](https://doc.rust-jp.rs/book-ja/ch01-03-hello-cargo.html)らしい

### clippy

[静的解析ツール](https://doc.rust-jp.rs/book-ja/appendix-04-useful-development-tools.html)らしい

### rust-docs

[日本語ドキュメント](https://doc.rust-jp.rs/)らしい

優しい。

### rust-std

[標準ライブラリ](https://doc.rust-lang.org/std/)らしい

### その他

[便利な開発ツール](https://doc.rust-jp.rs/book-ja/appendix-04-useful-development-tools.html)

フォーマッターとかあった。

## エディタ(VSCode)の設定

[こちらの記事](https://zenn.dev/23prime/articles/74cda5a096a3b3)を参考に導入する

language serverは、[rust-analyze](https://rust-analyzer.github.io/)が、いい感じらしい。

デバッガーは、[CodeLLDB](https://marketplace.visualstudio.com/items?itemName=vadimcn.vscode-lldb)がいいらしい

## Hello World

```sh
# create project
❯ cargo new intro-rust
     Created binary (application) `intro-rust` package

# build
❯ cargo build
   Compiling intro-rust v0.1.0 (/home/watashi-dev/work/repo/intro-rust)
    Finished dev [unoptimized + debuginfo] target(s) in 0.83s

# execute
❯ ./target/debug/intro-rust
Hello, world!

# one command run
❯ cargo run
    Finished dev [unoptimized + debuginfo] target(s) in 0.01s
     Running `target/debug/intro-rust`
Hello, world!

# build check(https://doc.rust-lang.org/book/ch01-03-hello-cargo.html)
❯ cargo check
    Finished dev [unoptimized + debuginfo] target(s) in 0.01s
```