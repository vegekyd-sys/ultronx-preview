# 星擎官网 · V 本地工作副本

来源：`https://www.ultronx.ai/`（2026-10-08 抓取）+ V 的改动。
用途：本地浏览 / 改内容 / 出补丁。

## 文件结构
```
index.html     首页（hero / 社媒矩阵 / 痛点 / AI Agent / 案例 / 团队 / 定价入口）
pricing.html   定价详情（★ V 已改：og 元信息 / ⓘ 点击展开 / 价格 webfont / 去掉底部空白）
product.html   产品页
images/        全部图片（已去掉 ?v= 查询串）
videos/        cloud-phone.mp4（首页/产品页用）
```

## 改内容改哪里
| 想改什么 | 去哪找 |
|---|---|
| 首页 hero 标题/副标题 | `index.html` → `.hero-title` / `.hero-subtitle` |
| 首页数字徽标（粉丝量等） | `index.html` → `.floating-badge` / `.badge-number` |
| 案例数据（播放量/线索/账号数） | `index.html`、`product.html` → `.case-stat-number` / `case-description` |
| 团队头像与姓名 | `index.html` → `images/何总.png`、`董力贤.png`、`谢蕾.png`、`大师.png` + `.agent-name` |
| 套餐价格与权益 | `pricing.html` → 三张卡片的 `data-plan="pro|pro-plus|max"` 区块 |
| 分享卡片文案 | `pricing.html` → `<meta property="og:*">` |

## 本地预览
```bash
cd site && python3 -m http.server 8080   # 然后浏览器打开 http://localhost:8080
```
直接双击 `index.html` 也能看，但页内跳转建议用上面的本地服务。

## 未包含
- 线上还有依赖 CDN 的资源（Tailwind CDN、Google Fonts），本地预览需要联网。
- 后端登录页 `https://xingqing.ultronx.tech/login` 是外链，不在副本内。
