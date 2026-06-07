# Ajazz Japan Landing - Codex 交接清单

## 项目部署链路

```
📁 本地目录: /home/xy_i/.openclaw/workspace/ajazz-japan-landing/
🐙 GitHub:    github.com/xieyee-dev/ajazz-japan-landing (main)
🚀 Vercel:    ajazz-japan-landing.vercel.app
```

**Vercel 已关联 GitHub main 分支**，push main 后约 30s 自动部署上线。

## 工作流程

```
1. 在本地目录修改代码
2. git add / git commit / git push origin main
3. Vercel 自动构建部署
4. 线上更新完成
```

## 已配好的 Git 配置

```bash
git config user.email "xieyee-dev@users.noreply.github.com"
git config user.name "xieyee-dev"
git remote origin: https://github.com/xieyee-dev/ajazz-japan-landing.git
```

## Git Push 注意事项

Codex 的 gh auth 可能未配置。如果 push 失败：

1. **方式一：** 找 Eric 要完整 token（`ghp_Bb…UNmD` 部分被遮挡），然后：
   ```bash
   echo "完整token" | gh auth login --hostname github.com --with-token
   ```
2. **方式二：** 让 Eric 手动跑一次 `git push` 就够了，之后 remote 会记住认证

## Eric 提出的升级需求

1. **增加 Amazon 购买链接** — 每个产品卡片加 "Amazonで購入" 按钮
2. **评估是否加 AliExpress 店铺链接** — 日本用户认知度不如 Amazon/楽天，优先级可低
3. **产品图片优化** — 替换为更接近电商平台风格的素材图，突出卖点和场景
4. **改完记得 git push 到 main** 触发 Vercel 自动部署

---

_创建日期: 2026-06-07_
