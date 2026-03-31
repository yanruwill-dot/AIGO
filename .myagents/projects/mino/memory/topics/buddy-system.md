# Buddy System - 电子宠物系统

## 概述

基于 Claude Code 泄露源码中的 Buddy System 彩蛋功能，创建了终端版和桌面版电子宠物系统。

## 技术细节

### 物种系统（18 种）
duck, goose, blob, cat, dragon, octopus, owl, penguin, axolotl, capibara, frog, hamster, rabbit, turtle, fox, panda, koala, hedgehog

### 稀有度系统
| 稀有度 | 概率 |
|--------|------|
| Common | 60% |
| Uncommon | 25% |
| Rare | 10% |
| Epic | 4% |
| Legendary | 1% |

### 特殊机制
- **闪光（Shiny）**：1% 概率，金色光环特效
- **Mulberry32 PRNG**：基于用户 ID 的确定性生成，与 Claude Code 源码相同

### 属性系统
DEBUGGING, PATIENCE, CHAOS, WISDOM, SNACK

### 配饰系统
crown, tophat, propeller, halo, wizard, beanie, tinyduck

## 文件位置

```
workspace/buddy-system/
├── buddy-term.py      # 终端宠物（Python）
├── DesktopBuddy.swift # 桌面宠物（Swift/AppKit）
├── build.sh           # 构建脚本
└── README.md          # 说明文档
```

## 使用方式

### 终端宠物
```bash
cd workspace/buddy-system
python3 buddy-term.py
```

### 桌面宠物
```bash
cd workspace/buddy-system
./build.sh
./DesktopBuddy  # 或 open DesktopBuddy.app
```

## 数据持久化

- 终端版：`~/.buddy_save.json`
- 桌面版：`~/.buddy_save.json`

## 状态

- 已完成基础功能
- Will 的宠物：Mino the Capibara 🦫（common, propeller 配饰）

## 下一步

- [ ] 添加更多互动功能
- [ ] 宠物动画效果
- [ ] 多宠物系统
