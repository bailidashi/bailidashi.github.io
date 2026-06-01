---
name: publish
description: 自动提交并上传网站到 GitHub
---

# Publish Skill

当用户输入 `/publish` 或要求发布网站时，自动将本地文件提交并推送到 GitHub。

## 行为

1. cd 到项目根目录 `D:\mygit\bailidashi.github.io`
2. 执行 `git status` 查看变更
3. 执行 `git add -A` 暂存所有修改
4. 根据变更内容自动生成简洁的中文 commit 信息
5. 执行 `git commit` 提交
6. 执行 `git push` 推送到 main 分支
7. 告知用户网站已发布，约 1-2 分钟后即可访问

## 注意事项

- 推送前确认用户意图，避免误提交敏感信息
- commit 信息需清晰描述本次变更内容
- 若 push 失败（如网络问题），告知用户具体错误并建议重试
