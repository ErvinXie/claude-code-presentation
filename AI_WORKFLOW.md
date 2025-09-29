# AI 工作流程规则

## 更新大纲工作流程

当用户更新内容时，请按以下步骤操作：

1. **检查变更**
   ```bash
   git diff
   ```
   获取最新的文件变更内容

2. **更新大纲**
   - 读取变更的内容
   - 将新内容合理地整合到 `presentation-outline.md` 中
   - 保持大纲结构的逻辑性和连贯性

3. **提交变更**
   ```bash
   git add .
   git commit -m "Update presentation outline with new content"
   ```

## 注意事项

- 每次更新都要保持大纲的整体结构
- 新内容应该与现有内容协调一致
- 提交信息要清晰描述变更内容
- 确保所有变更都被正确跟踪和保存

## 文件说明

- `presentation-outline.md`: 主要的演示大纲文件
- `from-human.md`: 用户输入的新内容
- `AI_WORKFLOW.md`: 本工作流程说明文件