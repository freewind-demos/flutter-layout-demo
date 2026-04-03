# Flutter 布局（Column + Expanded）

## 简介

竖向 `Column` 里三个 **`Expanded`**，等高瓜分垂直空间，分别填充红、绿、蓝。演示 Flex 家族最常用的「按比例吃剩余空间」。

## 快速开始

### 环境要求

Flutter SDK。

### 运行

```bash
flutter pub get
flutter run
```

## 概念讲解

### 第一部分：`Expanded` 与 `flex`

默认 `flex: 1` 三等分。若要 2:1:1，把第一个 `Expanded` 设 `flex: 2`。

### 第二部分：与 `Flexible`、`Spacer`

`Flexible` 允许子项小于最大约束；`Spacer` 本质是 `Expanded` 包空白。理解约束传递是读布局的关键。

## 完整示例

见 `lib/main.dart`：三色 `Container`。

## 注意事项

- `Column` 在无限高度约束（如 ListView 直插子节点）时会报错，需要 `Expanded`/`Flexible` 或改父级约束。
- 横排同理用 `Row`。

## 完整讲解（中文）

Flutter 布局第一句口诀：**先约束，后尺寸**。`Expanded` 说的是「在父给的最大范围内，我要抢一份弹性空间」。搞懂三桶颜色条，你再看复杂仪表盘，只是多叠几个 `Row/Column` 和 `Align`。
