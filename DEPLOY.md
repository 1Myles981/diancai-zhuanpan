# 点菜转盘 - 部署信息

## GitHub 部署
- **GitHub Pages**: https://1myles981.github.io/diancai-zhuanpan/
- **仓库**: https://github.com/1Myles981/diancai-zhuanpan
- **账号**: 1Myles981
- **本地 git remote**: `origin` → `https://github.com/1Myles981/diancai-zhuanpan.git`
- **Pages 配置**: Settings → Pages → master 分支, / (root)
- **推送命令**: `git push origin master`

## 文件说明
- `index.html` — 唯一源文件，本地开发编辑这个，同时也是 GitHub Pages 入口
- `DEPLOY.md` — 本文档

## 更新流程

### 方式一：git push（优先）
1. 修改 `index.html`
2. `git add index.html && git commit -m "描述修改内容" && git push origin master`
3. 等 1-2 分钟 GitHub Pages 自动部署，访问 https://1myles981.github.io/diancai-zhuanpan/ 验证

### 方式二：手动上传（网络不通时备用）
如果 git push 因网络问题失败，直接在 GitHub 网页操作：

1. 打开 https://github.com/1Myles981/diancai-zhuanpan
2. **更新 index.html**：点击文件列表里的 `index.html` → 右上角铅笔图标 ✏️（Edit this file）→ 全选删除旧内容 → 粘贴本地最新代码 → 点击绿色 "Commit changes..." 按钮 → 直接点 "Commit changes" 确认
3. **上传新文件**（如新增了图片）：点击 "Add file" 按钮 → "Upload files" → 拖入文件 → "Commit changes"
4. 等 1-2 分钟 GitHub Pages 自动部署，访问 https://1myles981.github.io/diancai-zhuanpan/ 验证

## 代码关键点
- **localStorage 键**: `dishwheel_recipes`(菜谱数组), `dishwheel_records`(每日记录)
- **分类**: meat(荤菜, #B85042), vegetable(素菜, #4A8C5C), soup(汤, #3D7EA6), other(其他, #8E6BAE)
- **背景图**: 内嵌为 base64 data URI（约 1.2MB），如需替换用 perl 命令写入
- **转盘 Canvas**: 尺寸 380×380，指针和 GO 按钮按比例缩放
- 无后端、无框架依赖，浏览器直接打开即可本地测试
- 每个设备 localStorage 独立，菜谱不跨设备共享
