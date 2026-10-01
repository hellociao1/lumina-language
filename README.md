# Lumina 流明语言

> 用自然语言写代码。多语法积木块、Comptime 元编程、从脚本到内核的统一系统级语言。

![Version](https://img.shields.io/badge/version-0.1.0--dev-blue)
![Python](https://img.shields.io/badge/python-3.12+-green)
![License](https://img.shields.io/badge/license-MIT-yellow)

## ✨ 特性

- **🗣️ 自然语言编程** — 用中文描述功能，编译器理解并生成 AST
- **🧩 多语法积木块** — natural_cn / zh_lumina / Python / Rust 风格混编
- **⚡ Comptime 元编程** — 编译期执行代码、静态断言、零开销元编程
- **🧠 三种内存模型** — safe / rc / manual，从应用到内核自由切换
- **🔒 三层安全** — full / min / none，编译期捕获内存错误
- **🚀 多后端** — LLVM 原生机器码、SPIR-V GPU、Wasm、裸机固件

## 🚀 快速开始

### 安装

```bash
git clone https://github.com/hellociao1/lumina-language.git
cd lumina-language
pip install -e .
```

### 运行

```bash
lumina run examples/hello.lu
```

### REPL

```bash
lumina repl
```

## 📝 语法示例

```lumina
-- 函数定义
func 求和(a: int, b: int) -> int {
  return a + b
}

-- 条件分支
if x > 10 {
  print("大于10")
} else {
  print("小于等于10")
}

-- 循环
for i in [1, 2, 3] {
  print(i)
}

-- 结构体
struct Point {
  x: int
  y: int
}
```

## 📁 项目结构

```
lumina-language/
├── src/lumina/           # 编译器核心
│   ├── ast.py            # AST 节点定义
│   ├── lexer.py          # 词法分析
│   ├── parser.py         # 语法解析
│   ├── interpreter.py    # NIR 解释器
│   └── cli.py            # 命令行工具
├── web/                  # GitHub Pages 在线演示
├── examples/             # 示例代码
└── tests/                # 测试
```

## 🗺️ 路线图

- [x] 词法分析器
- [x] AST 定义
- [x] 基础语法解析（函数、变量、if、for）
- [x] 内置解释器
- [x] CLI 工具
- [x] GitHub Pages 在线演示
- [ ] 完整类型系统
- [ ] Comptime 编译期执行
- [ ] SSA 中间表示
- [ ] 优化 Pass
- [ ] LLVM 后端
- [ ] natural_cn 自然语言解析
- [ ] 组件系统
- [ ] 借用检查器

## 📄 License

MIT
