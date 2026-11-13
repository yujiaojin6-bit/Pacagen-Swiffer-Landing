# GitHub Actions Workflow Maintenance Guide

## 目的
本文档记录了GitHub Pages部署工作流的维护信息，以防止未来的失败。

## 当前配置 (2026-11-13)

### GitHub Actions 版本
所有GitHub Actions均使用**最新稳定版本**：
- `actions/checkout@v4` (不是v3)
- `actions/configure-pages@v4` (不是v3)  
- `actions/upload-pages-artifact@v3` (不是v2)
- `actions/deploy-pages@v4` (不是v2)

⚠️ **重要**: GitHub已废弃v2和v3版本的某些actions。使用过期版本会导致部署失败。

## 常见问题和解决方案

### ❌ 问题：`deprecated version of actions/upload-artifact`
**原因**: 使用了过期的artifact action版本
**解决方案**: 
1. 将所有GitHub Actions升级到最新版本（v3+）
2. 在`.github/workflows/pages.yml`中检查版本号
3. 参考: https://github.blog/changelog/2024-04-16-deprecation-notice-v3-of-the-artifact-actions/

### ❌ 问题：GitHub Pages没有正确部署
**原因**: Pages设置未正确配置，或workflow失败导致部分步骤跳过
**解决方案**:
1. 检查GitHub Actions workflow运行日志
2. 确保GitHub Pages在repo settings中已启用
3. 检查deployment是否显示"success"（不仅仅是"completed"）

## 维护检查清单

### 每个月检查一次：
- [ ] 访问 `https://github.com/yujiaojin6-bit/Pacagen-Swiffer-Landing/actions`
- [ ] 查看最近的workflow runs是否都显示"success"
- [ ] 如果有任何"failure"，检查job logs并修复

### 当添加新的GitHub Actions时：
- [ ] 始终使用最新的稳定版本（v3+）
- [ ] 避免使用过期的action版本
- [ ] 在部署前在测试分支上验证workflow

### 自动化检查：
添加到workflow中的预防措施：
1. ✅ 使用最新版本的所有actions
2. ✅ 添加status checks以验证部署是否成功
3. ✅ 包含清晰的错误消息

## 部署验证

部署后，访问以下URL验证网站是否正常：
- 主网站: `https://yujiaojin6-bit.github.io/Pacagen-Swiffer-Landing/`
- 产品图片: `assets/product-*.png` 和 `assets/product-*.gif`
- 问题部分GIF: `assets/product-5.gif`

## 何时需要更新

GitHub Actions会定期发布新版本。注意以下标志：
- GitHub Actions标签上出现"deprecated"警告
- Workflow logs中出现"automatically failed"错误
- 部署失败但本地文件无问题

## 联系方式

如果workflow继续失败，请检查：
1. `.github/workflows/pages.yml` 中的action版本
2. GitHub Actions marketplace获取最新版本
3. GitHub Pages settings是否启用
