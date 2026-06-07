# Ajazz Landing Page — 产品图片升级执行记录

## 执行日期
2026-06-07

## 方法
从各产品 Rakuten 商品页的 og:image 取原图，ImageMagick resize 到 800×800，保存为 webp。

## 产品处理结果

| 产品 | 原图大小 | WebP 大小 | 来源 |
|---|---|---|---|
| AF84 | 168KB | **62KB** | Rakuten 商品页 |
| 308I | 365KB | **65KB** | Rakuten 商品页 |
| AK820-3 | 83KB | **57KB** | Rakuten 商品页 |
| N1 | 61KB | **16KB** | Rakuten 商品页 |
| AJ179 APEX | 340KB | **30KB** | Rakuten 商品页 |
| AK029 (猫鍵盤) | 89KB | **45KB** | Rakuten 商品页 |
| MK87 | 122KB | **52KB** | Rakuten 商品页 |
| AKP05 Pro | 53KB | **34KB** | Rakuten 商品页 |
| AK820 Pro | 162KB | **47KB** | Rakuten 商品页 |
| AK820 Max | 63KB | **35KB** | Rakuten 商品页 |
| AK820 Max Ultra | 180KB | **89KB** | Rakuten 商品页 |
| AKP815 | 176KB | **46KB** | Rakuten 商品页 |

全部 12 个产品成功，0 失败。

## 注意事项
- 图片统一 resize 到 800×800，保持宽高比
- WebP quality=85，JPG quality=90
- 图片文件直接替换 public/images/ 下对应文件
- i300 保留原有图片，已不在产品网格中使用

