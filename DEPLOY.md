# 点菜转盘 - 部署信息

## Gitee 部署（国内推荐）
- **仓库**: https://gitee.com/Myles981/diancai-zhuanpan
- **Gitee Pages**: https://myles981.gitee.io/diancai-zhuanpan
- **账号**: 远青 (Myles981)
- **本地 git remote**: `gitee` → `https://gitee.com/Myles981/diancai-zhuanpan.git`
- **推送命令**: `git push gitee master`
- **Pages 配置**: 服务 → Gitee Pages → master 分支, / 根目录

## GitHub 部署（备用，需 VPN）
- **仓库**: https://github.com/1Myles981/diancai-zhuanpan
- **GitHub Pages**: https://1myles981.github.io/diancai-zhuanpan/
- **账号**: 1Myles981
- **本地 git remote**: `origin` → `https://github.com/1Myles981/diancai-zhuanpan.git`
- **Pages 配置**: Settings → Pages → main 分支, / (root)

## 文件说明
- 本地开发文件: `点菜转盘.html`
- Pages 入口文件: `index.html`（两份内容相同，都需要）
- `DEPLOY.md`: 本文件

## 更新流程
1. 修改 `点菜转盘.html` 和 `index.html`（两个都要改）
2. 国内网直接 `git push gitee master`
3. Gitee Pages 会自动更新部署

## 技术要点
- 纯前端单文件，无后端，数据存 localStorage
- 4 分类：荤菜(meat)、素菜(vegetable)、汤(soup)、其他(other)
- 双模式：转盘 + 手动搭配
- 支持每日记录、批量导入、语音输入
- 背景图嵌入为 base64 data URI
