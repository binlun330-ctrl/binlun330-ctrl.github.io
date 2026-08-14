# 博客发布规则

这是“邦邦的乔布勒斯日记”的 GitHub Pages / Jekyll 仓库。

## 发布文章

当用户要求“发布到博客”时：

1. 在 `_posts/` 创建新的 Markdown 文件。
2. 文件名格式：
   `YYYY-MM-DD-英文短名.md`
3. Front Matter 使用：

   ```yaml
   ---
   title: 文章标题
   date: YYYY-MM-DD HH:MM:SS +0800
   category: 分类
   ---
   ```

4. 正文使用 Markdown。
5. 根据正文生成简短、稳定的英文文件名。
6. 默认不改动用户原意。
7. 只有用户明确要求润色时才润色。
8. 可以自动进行：
   - 合理分段
   - Markdown 标题层级
   - 列表
   - 引用
   - 加粗
9. 不要擅自修改：
   - `_config.yml`
   - `_layouts/`
   - `index.html`
   - `articles.html`
   - `about.html`

除非用户明确要求修改网站本身。

## 修改文章

修改已有文章时：

- 只修改对应 `_posts/` 文件。
- 尽量不要修改原文件名和发布日期，避免文章 URL 改变。

## 删除文章

删除文章时：

- 只删除对应 `_posts/` Markdown 文件。

## Git 工作流

完成文章操作后：

1. 运行 `git diff` 检查改动。
2. 确认没有无关文件被修改。
3. `git add`
4. `git commit`
5. `git push origin main`
6. 确认 push 成功。

默认使用快速发布：

- push 成功后立即向用户报告，不等待 GitHub Pages 构建完成。
- 不主动轮询 Pages 部署状态，也不主动访问线上页面验收。
- 只有用户明确要求“确认上线”“验证部署”或类似操作时，才等待构建并检查线上页面。

新文章的 commit message 格式：

`Publish: 文章标题`

修改文章：

`Update: 文章标题`

删除文章：

`Delete: 文章标题`
