# 简介
> Rust是一种令人兴奋的新编程语言,它可以让每个人编写可靠且高效的软件

Rust是一种通用的编程语言,但它更善于以下场景:
- 需要运行时的速度
- 需要内存安全
- 更好的利用多处理器

比如:
- 高性能的Web Service
- WebAssembly
- 命令行工具
- 网络编程
- 嵌入型设备
- 系统编程

# 安装
> 官网:https://www.rust-lang.org/

- 安装Rust: 请参考官网说明
- 更新Rust: rustup update
- 卸载Rust: rustup self uninstall
- 查看版本: rustc --version
- 本地文档: rustup doc

- 使用编辑器: 推荐vscode,  插件:rust-analyzer

# 基础入门
- 文件后缀名为rs,比如:main.rs
- 命名规范,小写英文单词,单词之间下划线分割,比如: hello_world.rs
- 编译: rustc hello_world.rs

```rust
fn main() {
    // 带!的是rust宏(Rust Marco)
    println!("hello world");
    // 不带!的是函数
    function()
}

fn function() {
    println!("Hello Rust Function");
}
```

- 运行Rust程序之前必须编译,编译成功后会生成一个二级制文件,可使用rustc命令以及cargo命令
- Rust是ahead-of-time编译的语言(可以先编译程序,然后把可执行文件交给别人运行,无需安装Rust)
- rustc只适合简单的程序,复杂的需要使用cargo(推荐使用cargo)
- cargo创建项目命令: cargo new [Project_name] , 比如: cargo new eromod
- 在Rust中,代码的包称作crate(※cargo的英文意思是货物, crate的英文意思是木箱)
- cargo build:  通过cargo构建项目文件
- cargo run:    通过cargo执行程序(先编译再执行)
- cargo check:  通过cargo执行代码检测,确保能通过编译,但是不产生编译文件(cargo check的速度比cargo build快的多,可连续反复通过cargo check来确包自己的代码能通过编译)
- cargo build --release: 通过cargo构建用于发布的程序,这种模式下的程序运行速度更快,但是编译时间更长

