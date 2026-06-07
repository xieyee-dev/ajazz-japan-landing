# 产品图片替换方案

## 现状 vs 乐天电商风格对比

### 当前落地页图片特点
- 图片尺寸不统一（800x533 到 1500x1500 到 4704x3136 都有）
- 产品图多为产品正面单角度拍摄，背景或白底或场景
- 没有统一视觉规范

### 乐天官方店图片特点
- **统一使用白底/纯色背景**
- **多角度展示**（正面、侧面、带灯效、带包装）
- **突出功能卖点**（TFT 屏幕特写、RGB 灯效、OLED 特写）
- **尺寸一致**，正方形构图（800x800 为主）
- **产品与环境融合**，有桌面场景搭配（键盘+鼠标+桌面布置）

## 具体替换建议

| 产品 | 当前图片问题 | 建议替换方向 | 乐天图来源 |
|------|-------------|-------------|-----------|
| **AF84** | 4704x3136 超大幅面，偏实拍 | 换 800x800 正方形白底产品图 | 商品详情页头图 |
| **308I** | 1200x900 实拍 | 换正方形白底+猫吸引眼球的角度 | 商品详情页头图 |
| **AK820-3** | 1200x900 实拍 | 换正方形白底+多颜色展示 | 商品详情页头图 |
| **AK820 Pro** | 800x800 白底 ✅ 可保留 | 可考虑加 TFT 屏幕特写版 | 商品详情页图2 |
| **AK820 Max** | 现有可用，偏暗 | 加 RGB 灯效展示图 | 商品详情页 |
| **AK820 Max Ultra** | 现有可用 | 换带灯效+桌面场景图 | 商品详情页 |
| **MK87** | 1200x1200 白底 ✅ 可保留 | 加 TFT 屏幕亮起特写 | 商品详情页 |
| **AJ179 APEX** | 1500x1500 ✅ 偏暗 | 换带 OLED+充电底座特写的白底图 | 商品详情页头图 |
| **N1** | 800x800 ✅ 可保留 | 加带按键灯光特写的图 | 商品详情页 |
| **AKP05 Pro** | 现有 | 加 LCD 屏幕亮起特写 | 商品详情页 |
| **AKP815** | 现有 | 加 LCD 大屏亮起特写 | 商品详情页 |
| **AK029** | 现有 | 换更清晰的猫键帽特写 | 商品详情页 |

## 尺寸规范建议

所有产品图统一为 **800x800 正方形**，WebP 格式：
```
public/images/{product_id}.webp  →  800×800, WebP
public/images/{product_id}.jpg   →  800×800, JPEG（fallback）
```

## 优先级

1. **最高**：AF84、308I、AK820-3（尺寸不统一，明显偏离）
2. **高**：AJ179 APEX、AK029（现有图偏暗/模糊）
3. **中**：MK87、AK820 Pro、AK820 Max Ultra（可优化但现有还行）
4. **低**：N1、AKP05 Pro、AKP815（现有图可用）

## 实施方式

**由 Codex 实现**：
1. 从各乐天商品详情页抓取头图（右键复制或 API 下载）
2. 统一 resize 到 800×800
3. 替换 `public/images/` 下对应文件
4. 更新 `app/page.tsx` 中如有尺寸相关样式
5. git push → Vercel 自动部署

## 乐天商品页链接（直接获取头图）

- https://item.rakuten.co.jp/ajazz/af84/
- https://item.rakuten.co.jp/ajazz/308i/
- https://item.rakuten.co.jp/ajazz/ak820-3/
- https://item.rakuten.co.jp/ajazz/ak820pro/
- https://item.rakuten.co.jp/ajazz/ak820max/
- https://item.rakuten.co.jp/ajazz/ak820maxultra/
- https://item.rakuten.co.jp/ajazz/mk87/
- https://item.rakuten.co.jp/ajazz/aj179apex/
- https://item.rakuten.co.jp/ajazz/n1/
- https://item.rakuten.co.jp/ajazz/akp05pro/
- https://item.rakuten.co.jp/ajazz/akp815/
- https://item.rakuten.co.jp/ajazz/ak029-mt/
