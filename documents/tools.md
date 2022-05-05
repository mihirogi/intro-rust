# tools

## formatter

[rustfmtを使った自動フォーマット](https://doc.rust-jp.rs/book-ja/appendix-04-useful-development-tools.html#:~:text=%E3%81%A6%E3%81%84%E3%81%8D%E3%81%BE%E3%81%99%E3%80%82-,rustfmt%E3%82%92%E4%BD%BF%E3%81%A3%E3%81%9F%E8%87%AA%E5%8B%95%E3%83%95%E3%82%A9%E3%83%BC%E3%83%9E%E3%83%83%E3%83%88,-rustfmt%E3%81%A8%E3%81%84%E3%81%86%E3%83%84%E3%83%BC%E3%83%AB)

```sh
❯  rustup component add rustfmt
info: component 'rustfmt' for target 'x86_64-unknown-linux-gnu' is up to date

❯  cargo fmt # 特に表示はないけどできてた

# 差分があるとき
❯  cargo fmt --check
Diff in /home/watashi-dev/work/repo/intro-rust/src/main.rs at line 1:
-fn main() { println!("Hello, world!");
+fn main() {
+    println!("Hello, world!");
 }
```