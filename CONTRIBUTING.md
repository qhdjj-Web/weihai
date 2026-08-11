# 🤝 贡献指南

感谢你对本项目的兴趣！欢迎提交 Issue 和 Pull Request。

## 如何报告 Bug

1. **检查问题是否已存在**
   - 在 Issues 中搜索关键词
   - 查看已关闭的 Issue

2. **创建新 Issue**
   - 标题：简洁描述问题
   - 描述：详细信息
   - 环境：浏览器型号、版本
   - 复现步骤：如何重现问题
   - 预期效果 vs 实际效果

### Bug 报告模板
```markdown
## 问题描述
<!-- 简要说明问题 -->

## 复现步骤
1. 
2. 
3. 

## 预期效果
<!-- 应该发生什么 -->

## 实际效果
<!-- 实际发生了什么 -->

## 环境信息
- 浏览器：Chrome 120
- 操作系统：Windows 11
- 其他：...
```

## 功能建议

有好的想法？分享给我们！

1. **创建 Discussion**
   - 打开项目 Discussions
   - 选择"Ideas"分类
   - 描述你的想法和为什么需要这个功能

2. **讨论改进方案**
   - 社区成员会参与讨论
   - 获得反馈和建议

## 提交代码

### 准备工作

1. **Fork 项目**
   ```bash
   # 在 GitHub 上 Fork 本仓库
   ```

2. **克隆你的 Fork**
   ```bash
   git clone https://github.com/YOUR_USERNAME/weihai-tour-planner.git
   cd weihai-tour-planner
   ```

3. **创建功能分支**
   ```bash
   git checkout -b feature/your-feature-name
   # 或 bug fix 分支
   git checkout -b fix/issue-description
   ```

### 开发规范

#### 代码风格
- 使用 2 空格缩进
- 变量名使用驼峰命名法：`newSpotName`
- 函数名使用驼峰命名法：`loadSpots()`
- 添加必要的注释

#### 提交信息
```
详细改进说明或修复的问题
[功能类型] 简要描述

类型可以是：
- feat: 新功能
- fix: 修复 bug
- docs: 文档更新
- style: 代码风格调整
- refactor: 代码重构
- test: 测试相关
```

示例：
```
[feat] 添加景点收藏功能
[fix] 修复地图标记不显示的问题
[docs] 更新 README 使用说明
```

#### 测试
- 在多个浏览器中测试（Chrome、Firefox、Safari、Edge）
- 在不同屏幕尺寸上测试
- 测试导出/导入功能
- 测试 localStorage 数据持久化

### 提交 Pull Request

1. **推送到你的 Fork**
   ```bash
   git push origin feature/your-feature-name
   ```

2. **打开 Pull Request**
   - 目标分支：`main`
   - 标题：简要描述改变内容
   - 描述：使用下面的模板

### PR 模板
```markdown
## 描述
<!-- 这个 PR 做了什么改变？ -->

## 关联问题
Closes #<issue-number>

## 改动类型
- [ ] Bug 修复
- [ ] 新功能
- [ ] 文档更新
- [ ] 代码重构

## 测试清单
- [ ] 已在 Chrome 中测试
- [ ] 已在 Firefox 中测试
- [ ] 已在 Safari 中测试
- [ ] 已测试导出/导入功能
- [ ] localStorage 数据正常保存

## 截图/演示
<!-- 如果适用，上传截图或 GIF -->

## 其他信息
<!-- 任何其他相关信息 -->
```

## 文档贡献

改进文档也很重要！

1. **编辑文件**
   - README.md：主项目说明
   - docs/FEATURES.md：功能详细说明
   - docs/GUIDE.md：使用指南

2. **提交 PR**
   - 遵循上述流程
   - 确保 Markdown 格式正确

## 翻译贡献

欢迎翻译成其他语言！

1. **创建语言分支**
   ```bash
   git checkout -b i18n/language-code
   # 例如：i18n/es（西班牙语）、i18n/ja（日语）
   ```

2. **创建翻译文件**
   ```
   docs/
   ├── README.md（英文）
   ├── README.zh-CN.md（中文）
   ├── README.es.md（西班牙文）
   └── ...
   ```

3. **提交 PR**
   - 标题：`[i18n] 翻译说明`

## 项目维护

### 发布新版本

版本号遵循 [Semantic Versioning](https://semver.org/)：
- MAJOR：不兼容的改变（X.0.0）
- MINOR：向后兼容的新功能（x.Y.0）
- PATCH：向后兼容的 bug 修复（x.y.Z）

### Commit 历史保持整洁
- 避免混乱的 merge commit
- 使用 `git rebase` 整理历史
- 每个 commit 应该是有意义的单位

## 行为准则

我们承诺提供一个热情、安全和包容的社区。

### 我们的承诺
- 尊重所有贡献者和用户
- 欢迎各种背景和经验水平的参与
- 构建一个鼓励和建设性的社区

### 不可接受的行为
- 骚扰、威胁或冒犯性语言
- 性骚扰或歧视
- 侵犯他人隐私
- 恶意或破坏性行为

### 举报问题
如果遇到不符合行为准则的情况，请通过邮件报告。

## 常见问题

### Q：首次贡献应该从哪里开始？
A：查看 Issues 中标记为 `good first issue` 的问题，或完善文档。

### Q：我的 PR 被拒绝了怎么办？
A：维护者会提供具体反馈，您可以：
1. 讨论改进建议
2. 按反馈修改
3. 重新提交

### Q：多长时间才能得到回复？
A：通常 1-2 周内，但可能因维护者繁忙延长。

### Q：可以对已提交的 PR 继续修改吗？
A：可以，继续 push 到同一分支即可。

## 联系方式

- **Issues**：报告 bug 和功能建议
- **Discussions**：讨论问题和想法
- **Email**：[your-email@example.com]

---

感谢你的贡献！🎉

这个项目因为你们变得更好。
