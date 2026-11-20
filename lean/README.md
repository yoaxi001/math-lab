# lean/

Lean 4 工程，采用**单包多模块**布局：一个 `lakefile.toml`，每道题是 `MathProof/ProblemNNN.lean` 一个模块。

## 当前状态：尚未安装工具链

本机还没有 `lean` / `lake` / `elan`，所以这个目录现在不能构建。
`lean-toolchain` 是**故意没有创建**的 —— 等装好工具链后由 elan 生成，避免写一个本机并不存在的版本号。

## 装好后怎么用

1. 安装 elan（Lean 版本管理器），参考官方 Getting Started
2. 在本目录执行 `lake build`，第一件事是确认 `MathProof.Basic` 能编译
3. 再把每道题写成 `MathProof/ProblemNNN.lean`

## Mathlib

`lakefile.toml` 里 Mathlib 依赖是注释掉的。需要时取消注释再 `lake update`，
注意首次下载量大。