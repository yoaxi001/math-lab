# math-lab

数学难题的推演记录与 Lean 形式化验证。一个仓库装所有题目，用 `problems/` 下的文件夹分类。

> 本仓库只收录从 2026-11 起的新题目。此前的数学内容仍是各自独立的仓库：
> - triangle-bisector-median-inequality（本地 `..\liu51_proof`）
> - polygon-sixth-distance-moment（本地 `..\polygon-sixth-distance-moment`）
> - math-projects

## 目录结构

```
math-lab/
├── README.md              本文件，兼索引
├── problems/              一道题一个文件夹
│   └── _template/         新题目从这里复制
├── lean/                  Lean 4 工程（单包多模块）
│   ├── lakefile.toml
│   └── MathProof/         每题一个 .lean 模块
└── .gitignore
```

## 新建一道题

1. 复制 `problems/_template/` 为 `problems/YYYY-MM-DD-主题/`
2. 填 `statement.md`（题目原文与出处）和 `reasoning.md`（**有效的**推演链，不是和 AI 的往返记录）
3. 在 `lean/MathProof/` 下建 `ProblemNNN.lean`，编号与题目一致
4. 在下表加一行
5. 提交

## 索引

| 编号 | 题目 | 主题 | 状态 |
| --- | --- | --- | --- |
| — | （还没有题目） | — | — |

## 命名约定

- 文件夹：`YYYY-MM-DD-短横线主题`，例如 `2026-11-20-cauchy-schwarz`
- Lean 模块：`Problem001`、`Problem002` …… 按加入顺序，三位补零
- 状态取值：`草案` / `推演完成` / `形式化中` / `已验证` / `放弃`