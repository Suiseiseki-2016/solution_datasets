# 输出结果目录

这个目录包含最终批量处理的所有结果文件。

## 📁 目录结构

```
output_results/
├── README.md                                    # 本说明文件
├── final_batch_merged_solutions_时间戳.json     # 合并后的题解数据
├── final_batch_final_result_时间戳.json         # 最终综合结果
├── final_batch_processing_stats_时间戳.json     # 处理统计信息
├── wenjiajia_index_时间戳.json                  # 问佳佳格式索引文件
├── wenjiajia_batch_0000_时间戳.json            # 问佳佳格式第1个batch
├── wenjiajia_batch_0001_时间戳.json            # 问佳佳格式第2个batch
├── ...                                         # 更多batch文件
└── wenjiajia_batch_0072_时间戳.json            # 问佳佳格式最后一个batch
```

## 📊 文件说明

### 1. 合并后的题解数据
- **文件名**: `final_batch_merged_solutions_时间戳.json`
- **内容**: 从多个数据源合并的完整题目信息
- **格式**: 包含题目信息、tutorial、代码示例等

### 2. 最终综合结果
- **文件名**: `final_batch_final_result_时间戳.json`
- **内容**: 包含元数据和合并后的题解
- **用途**: 完整的数据集概览

### 3. 处理统计信息
- **文件名**: `final_batch_processing_stats_时间戳.json`
- **内容**: 处理过程的详细统计
- **包含**: 成功/失败数量、处理时间、数据源统计等

### 4. 问佳佳格式文件
- **索引文件**: `wenjiajia_index_时间戳.json`
  - 所有batch的索引信息
  - 每个batch包含的题目列表
  
- **Batch文件**: `wenjiajia_batch_XXXX_时间戳.json`
  - 每个batch最多包含100个题目
  - 标准化的问佳佳v1.0格式
  - 包含题目信息、解决方案、代码示例等

## 🎯 问佳佳格式特点

- **标准化**: 统一的数据结构
- **分batch**: 便于管理和使用
- **完整性**: 包含所有必要信息
- **可扩展**: 支持后续功能扩展

## 📈 使用建议

1. **查看索引**: 先查看`wenjiajia_index_时间戳.json`了解整体结构
2. **按需加载**: 根据需要的题目范围加载对应的batch文件
3. **批量处理**: 可以并行处理多个batch文件
4. **数据验证**: 使用索引文件验证数据的完整性

## 🔄 更新说明

- 每次运行会生成新的时间戳文件
- 旧文件保留，便于对比和回滚
- 建议定期清理过期的输出文件
