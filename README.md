# 题解提取器 - 精简版

## 📁 目录结构

```
data_process/
├── README.md                           # 主说明文档
├── README_simple_extractor.md          # 精简版提取器详细说明
├── simple_solution_extractor.py        # 🎯 核心：精简版题解提取器
├── extraction_results/                 # 📊 精简版提取结果
├── current_problem_tutorials/          # 📚 当前题目tutorial结果（旧版本）
├── model_cache/                        # 🤖 AI模型缓存
├── final_output/                       # 📥 最终数据输入
└── __pycache__/                        # 🐍 Python缓存文件
```

## 🎯 核心功能

这个精简版本只包含两个核心功能：

1. **获取题目内容**：从两个数据集中提取指定题目的所有内容
2. **AI 提取题解**：使用 AI 从内容中提取出题解原文

## 🚀 快速开始

### 1. 运行精简版提取器
```bash
uv run python simple_solution_extractor.py
```

### 2. 修改题目ID
在 `simple_solution_extractor.py` 的 `main()` 函数中修改：
```python
problem_id = "1418/G"  # 改为你想要的题目ID
```

### 3. 查看结果
结果会保存在 `extraction_results/` 目录中，包含：
- `*_content.json` - 题目内容数据
- `*_solution.json` - 题解提取结果
- `*_solution.txt` - 纯文本格式的题解

## 📊 清理说明

我们已经清理了以下复杂且不再需要的文件：
- ❌ 复杂的旧版本提取器（40+ 文件）
- ❌ 多个演示和测试脚本
- ❌ 复杂的结果展示工具
- ❌ 旧的配置和文档文件

## 💡 优势

- **代码简洁**：从 800+ 行精简到 394 行
- **功能聚焦**：只有两个核心功能，逻辑清晰
- **易于维护**：代码结构简单，易于理解和修改
- **高效运行**：处理速度快，内存占用少

## 🔧 配置选项

- **model_version**: "7B" 或 "13B"
- **use_ai**: 是否启用 AI 功能
- **data_file**: 数据文件路径

## 📚 详细文档

更多详细信息请查看 `README_simple_extractor.md`。

---

**注意**：`current_problem_tutorials/` 目录包含旧版本的测试结果，如果需要可以删除。
# solution_datasets
