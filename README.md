# 龙珠连连看 · Dragon Ball Link Game

一个七龙珠主题的连连看网页小游戏,纯 HTML/CSS/JS 单文件实现,无需任何后端,可直接部署到 Vercel。

## 玩法

- 点击两张**相同**的卡牌,如果它们之间的连线**拐弯不超过 2 次**,即可消除
- 消除全部 24 对卡牌即获胜:七颗龙珠全部点亮,召唤神龙 🐉
- 每消除约 1/7 的卡牌,就会点亮一颗龙珠
- 💡 提示:扣 5 分 | 🔀 洗牌:扣 10 分 | 🔥 连击有加分 | 剩余时间转化为奖励分

## 本地运行

直接用浏览器打开 `index.html` 即可。

## 部署到 GitHub + Vercel(课程作业步骤)

### 第一步:上传代码到 GitHub

```bash
# 进入项目文件夹
cd dragon-ball-link-game

# 告诉 Git:这里要变成仓库
git init

# 把所有文件打包
git add .

# 贴快递单:写备注
git commit -m "龙珠连连看初始版本"

# 连接 GitHub 仓库(把"你的用户名"换成真的,先在 github.com 新建一个空仓库)
git remote add origin https://github.com/你的用户名/dragon-ball-link-game.git

# 发车!
git push -u origin main
```

⚠️ 常见翻车点:
- 弹出浏览器授权窗口,点 **Authorize** 即可
- 提示 failed to push → 检查远程仓库地址是否打错
- 分支名是 master 不是 main → 先 `git branch -M main` 再 push
- 老师要求**至少 3 次 commit**,可以分多次提交(初始版本 → 加功能 → 写 README)

### 第二步:Vercel 一键上线

1. 打开 [vercel.com](https://vercel.com),Sign Up → **Continue with GitHub**
2. 点击 **Add New Project** → 找到 `dragon-ball-link-game` 仓库 → **Import**
3. Framework Preset 选 **Other**(纯 HTML,不要选 Next.js)
4. 点击 **Deploy** → 等待约 1 分钟 → 获得 `xxx.vercel.app` 网址

✅ 成功标志:把网址发到手机微信,能打开能玩,就是真的上线了!

## 技术说明

- 单文件 `index.html`,零依赖、零构建
- 连连看核心算法:带外圈扩展网格的 BFS,限制拐弯数 ≤ 2
- 12 种龙珠主题卡牌:悟空、贝吉塔、龟仙人、神龙、筋斗云……
