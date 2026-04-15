# AtlasMesh Quant

🌐 语言：
[English](README.md) | [中文](README.zh.md)

---

## 🚀 概述

**AtlasMesh Quant** 是一个面向加密市场（数字资产）的 AI 量化交易系统，基于 Microsoft Qlib 扩展，强调：

- 研究→实盘的完整链路
- 策略回测与参数优化
- 实时执行与风控
- Web 仪表盘可视化

---

## ✨ 功能

- AI/机器学习策略研究（Qlib）
- Binance / OKX / Bybit（可扩展）
- 回测 + 参数优化
- 实时交易执行引擎
- 风险控制模块（仓位/回撤/频率）
- Streamlit Web 仪表盘

---

## ⚡ 快速开始

```bash
pip install -r requirements.txt
python quant_framework.py
streamlit run dashboard.py
```

访问: http://localhost:8501

---

## 🧩 开发策略

```python
class MyStrategy(Strategy):
    def __init__(self):
        super().__init__("My Strategy", "BTCUSDT", "1h")

    def calculate_signal(self, df):
        # your signal
        return signal
```

---

## 🗺️ 状态

- 当前：仓库初始化
- 计划：增加示例策略、回测用例、仪表盘模板

---

## 📚 文档

- [docs/workflow.md](docs/workflow.md)（完整工作流 + 学习路线）
- quantitative_trading_guide.md（你本地 /Users/laok/Documents/GitHub/qlib 中的介绍与使用方法，上传后合并）
