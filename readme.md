# 显卡性价比分析工具

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

> 交互式散点图：天梯分数 vs 市场价格，自动计算趋势线，高亮高性价比显卡。

![截图示例](screenshot.png)

## 在线演示

👉 [点击使用工具](https://your-username.github.io/GPU-Price-Performance-Chart/) *(实际链接请替换)*

## 主要功能

- 📊 **散点图**：纵轴为性能分数，横轴为价格（**对数坐标** – 低价区间点不再重叠）
- 📈 **市场趋势线**（对价格取对数后的线性回归）+ **理想 1:1 性价比参考线**
- ⭐ **自动高亮**：性价比高于平均线 10% 以上的显卡
- 🔍 **悬浮工具窗**：显示完整规格、分数、价格、偏离趋势线的距离
- 📁 **上传自定义 JSON 数据**：用自己的跑分和实时价格重新绘图
- 🧮 **数据表格**：按性价比排序，支持快速查看推荐产品
- 🎨 **深色主题**，响应式布局

## 使用方法

1. 用现代浏览器打开 `index.html`（或部署到 GitHub Pages）。
2. 默认加载最新显卡数据（含价格估算）。
3. **交互操作**：
   - 鼠标悬浮在点上 → 显示详细信息
   - 点击 **“仅显示高性价比”** → 只显示推荐显卡
   - 点击 **“数据表格”** → 查看按性价比排序的表格
4. **使用自己的数据**：
   - 准备 JSON 文件（格式见下文）
   - 点击 **“上传JSON数据”** → 选择文件 → 图表自动更新

## 数据格式

JSON 文件必须符合以下结构：

```json
{
  "gpus": [
    {
      "name": "NVIDIA GeForce RTX 4070",
      "memory": "12GB GDDR6X",
      "release": "2023.04",
      "score": 17887,
      "price": 4200
    }
  ]
}