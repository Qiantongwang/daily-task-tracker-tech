# 每日任务 & 执行水平 Tracker

一个轻量、美观、**完全本地运行**的每日任务记录网站。

**在线演示**（部署后替换成你的地址）：  
`https://你的用户名.github.io/daily-task-tracker/`

## 功能亮点

- ✅ 按日期管理任务（支持前后翻天、一键回到今天）
- ✅ 状态标记：待办 / 进行中 / 已完成 / 未完成 / 取消（带颜色徽章）
- ✅ 优先级：高 / 中 / 低
- ✅ **执行水平评分**（1–5 星），完成任务后可对执行质量打分
- ✅ 分类标签、备注
- ✅ 今日完成率圆环 + 统计卡片
- ✅ 近期历史记录（点击可跳转）
- ✅ 数据保存在浏览器 `localStorage`，**不上传任何服务器**
- ✅ 一键导出当天 JSON
- ✅ 首次打开会自动导入示例任务

## 快速部署到 GitHub Pages

### 方法一：网页操作（推荐新手）

1. 打开 [GitHub](https://github.com) 并登录
2. 点击右上角 **+** → **New repository**
3. 仓库名填写：`daily-task-tracker`（或任意名字）
4. 选择 **Public**
5. **不要**勾选 “Add a README file”
6. 点击 **Create repository**
7. 在仓库页面点击 **uploading an existing file**
8. 把本目录下的 `index.html` 和 `README.md` 拖进去
9. 点击 **Commit changes**
10. 进入仓库 **Settings** → 左侧 **Pages**
11. Source 选择 **Deploy from a branch**
12. Branch 选择 `main`，文件夹选 `/ (root)`
13. 点击 **Save**
14. 等待 1–2 分钟，页面会显示你的网站地址：  
    `https://你的用户名.github.io/daily-task-tracker/`

### 方法二：命令行（已安装 Git）

```bash
# 1. 进入本项目目录
cd daily-task-tracker

# 2. 初始化并提交
git init
git add .
git commit -m "Initial commit: Daily Task Tracker"

# 3. 关联你的仓库（把下面地址换成你自己的）
git branch -M main
git remote add origin https://github.com/你的用户名/daily-task-tracker.git
git push -u origin main
```

然后同样去仓库 **Settings → Pages** 开启 Pages 即可。

## 本地预览

```bash
# 直接打开
open index.html          # macOS
start index.html         # Windows

# 或起本地服务器
python3 -m http.server 8080
# 访问 http://localhost:8080
```

## 数据说明

- 所有任务数据只保存在你当前浏览器的 `localStorage` 中
- 不同设备 / 不同浏览器之间**不会自动同步**
- 建议定期点击页面上的「导出」按钮备份 JSON
- 换电脑后重新导入即可继续使用

## 技术栈

纯前端单文件：HTML + CSS + 原生 JavaScript，无任何框架依赖。
