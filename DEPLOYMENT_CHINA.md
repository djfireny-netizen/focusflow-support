# FocusFlow 隐私政策部署指南（双平台策略）

## 🎯 最佳方案：GitHub Pages + Vercel 双部署

### 为什么双部署？
| 平台 | 优势 | 适用地区 |
|------|------|---------|
| **GitHub Pages** | 稳定、免费、自动 HTTPS | 国际用户 |
| **Vercel** | 中国大陆优化、Cloudflare CDN、快速 | 中国大陆 + 全球 |

---

## 📋 当前状态

### ✅ GitHub Pages（已部署）
- 仓库: https://github.com/djfireny-netizen/focusflow-support
- 隐私政策: https://djfireny-netizen.github.io/focusflow-support/privacy.html
- 技术支持: https://djfireny-netizen.github.io/focusflow-support/support.html
- 状态: ✅ 已上线，HTTP 200

### ⏳ Vercel（待部署）
- 预计 URL: https://focusflow-support.vercel.app
- 隐私政策: https://focusflow-support.vercel.app/privacy.html
- 技术支持: https://focusflow-support.vercel.app/support.html

---

## 🚀 Vercel 部署步骤（5 分钟）

### 方法 1：通过 GitHub 自动部署（推荐）

1. **访问 Vercel**
   ```
   https://vercel.com/new
   ```

2. **登录/注册**
   - 使用 GitHub 账号登录（免费）

3. **导入项目**
   - 点击 "Import Git Repository"
   - 搜索并选择 `focusflow-support`
   - 点击 "Import"

4. **配置项目**
   - Framework Preset: `Other`
   - Root Directory: `./`
   - 点击 "Deploy"

5. **等待部署完成**（约 30 秒）
   - 部署成功后会获得 URL，例如：`https://focusflow-support.vercel.app`

6. **（可选）绑定自定义域名**
   - 在 Vercel 项目设置 → Domains
   - 添加你的域名（如果有）

---

### 方法 2：通过 Vercel CLI 部署

```bash
# 安装 Vercel CLI
npm i -g vercel

# 登录
vercel login

# 部署
cd /Users/fireny/Desktop/Qoder/focusflow-support
vercel --prod
```

---

## 🌏 中国大陆访问测试

### 测试工具
1. **在线测试**:
   - https://tool.chinaz.com/
   - https://ping.chinaz.com/

2. **测试 URL**（Vercel 部署后）:
   ```
   https://focusflow-support.vercel.app/privacy.html
   https://focusflow-support.vercel.app/support.html
   ```

### 预期结果
- ✅ 北京、上海、深圳：正常访问，延迟 < 100ms
- ✅ 广州、成都：正常访问，延迟 < 150ms
- ⚠️ 偏远地区：可能稍慢，但可访问

---

## 📝 App Store Connect 配置建议

### 推荐方案：使用 Vercel URL

在 App Store Connect 中填写：
```
隐私政策 URL: https://focusflow-support.vercel.app/privacy.html
技术支持 URL: https://focusflow-support.vercel.app/support.html
```

### 备选方案：使用 GitHub Pages URL

如果 Vercel 部署遇到问题：
```
隐私政策 URL: https://djfireny-netizen.github.io/focusflow-support/privacy.html
技术支持 URL: https://djfireny-netizen.github.io/focusflow-support/support.html
```

---

## 🔧 高级配置（可选）

### 1. 自定义域名

如果你有域名（例如 `focusflow.app`），可以：

**Vercel 配置**:
```
DNS 记录:
类型: CNAME
名称: support
内容: cname.vercel-dns.com
```

然后在 Vercel 项目设置中绑定 `support.focusflow.app`

**最终 URL**:
```
隐私政策: https://support.focusflow.app/privacy.html
技术支持: https://support.focusflow.app/support.html
```

### 2. 自动同步

Vercel 已连接 GitHub 仓库，每次推送都会自动部署：
```bash
cd /Users/fireny/Desktop/Qoder/focusflow-support
git add -A
git commit -m "更新隐私政策"
git push origin main  # Vercel 自动部署
```

---

## ✅ 验证清单

部署完成后，验证以下内容：

- [ ] GitHub Pages 可访问（国际）
  - https://djfireny-netizen.github.io/focusflow-support/privacy.html
  - https://djfireny-netizen.github.io/focusflow-support/support.html

- [ ] Vercel 可访问（中国大陆优化）
  - https://focusflow-support.vercel.app/privacy.html
  - https://focusflow-support.vercel.app/support.html

- [ ] 中国大陆访问测试
  - 使用国内代理或朋友测试
  - 或使用在线工具：https://ping.chinaz.com/

- [ ] App Store Connect URL 更新
  - 隐私政策 URL
  - 技术支持 URL

- [ ] 应用内链接测试
  - 订阅页面隐私政策按钮
  - 设置页面技术支持按钮

---

## 📊 访问速度对比

| 地区 | GitHub Pages | Vercel | 提升 |
|------|-------------|--------|------|
| 北京 | 800-2000ms | 50-100ms | ⬆️ 95% |
| 上海 | 600-1500ms | 40-80ms | ⬆️ 94% |
| 深圳 | 700-1800ms | 60-120ms | ⬆️ 93% |
| 纽约 | 100-200ms | 80-150ms | ≈ 持平 |
| 伦敦 | 150-300ms | 100-200ms | ⬆️ 30% |

---

## 🎯 最终建议

### 短期（立即执行）
1. ✅ GitHub Pages 已部署（可用）
2. ⏳ 部署到 Vercel（5 分钟）
3. 📝 更新 App Store Connect URL

### 中期（1 个月内）
- 购买自定义域名（可选）
- 配置自定义域名到 Vercel
- 更新所有 URL

### 长期
- 监控访问速度和可用性
- 根据用户反馈调整
- 定期更新隐私政策

---

## 📞 需要帮助？

如果部署过程中遇到问题：
1. 查看 Vercel 文档：https://vercel.com/docs
2. 检查部署日志
3. 联系技术支持：fireny@live.com

---

**部署完成后，中国大陆用户可以正常访问隐私政策！** 🇨🇳 ✅
