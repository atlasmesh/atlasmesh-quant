# AtlasMesh Quant 文档

🌐 语言：[English](README.md) | [中文](README.zh.md)

---

## 🚀 完整量化交易工作流

### 🤍 Step 1：理论学习
- 阅读 `quantitative_trading_guide.md`
- 了解因子/分析、回测、风控的基础

### ⚡ Step 2：运行框架演示
推荐使用 virtualenv（粒粒机细粒和认真负责）

```bash
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python quant_framework.py
```

运行后会：
- 获取数据
- 回测多种策略
- 参数优化
- 输出性能指标

### 📊 Step 3：启动 Web 仪表盘
先确认安装 `streamlit`：

```bash
pip install streamlit
streamlit run dashboard.py
```

访问： http://localhost:8501

#### 仪表盘内容
- 📈 行情图表
- 📋 空仓/帐户信息
- 💡 交易信号

### 🐎 Step 4：自己开发策略
编辑 `quant_framework.py`，继承 `Strategy` 类：

```python
class MyStrategy(Strategy):
    def __init__(self):
        super().__init__("我的策略", "BTCUSDT", "1h")

    def calculate_signal(self, df):
        # 你的策略逻辑
        signal = ...
        return signal

    def get_description(self):
        return "我的策略描述"

# 回测
strategy = MyStrategy()
backtester = Backtester(strategy)
results = backtester.run(df)
backtester.print_results(results)
```

---

## 📚 推荐学习路线

### 第 1 周：基础
- Day 1-2：阅读 `quantitative_trading_guide.md`
- Day 3-4：运行 `quant_framework.py`，了解回测逻辑
- Day 5-7：在仪表盘上分析信号

### 第 2 周：实践
- Day 1-3：修改 MA 参数，观察性能
- Day 4-5：优化参数组合（5-30, 15-50）
- Day 6-7：模拟运行

### 第 3-4 周：验证
- 运行 48+ 小时，监控策略
- 调整参数，再验证 1-2 周

### 第 5+ 周：实盘
- 移到主网
- 小额资金（100-500元）
- 严格风控

---

## 👉 核心概念速查

什么是好策略？
- ✅ 有逻辑基础，能解释为什么这样做
- ✅ 数据支撑，历史回测有效
- ✅ 风险可控，最大回撤 < 20%
- ✅ 胜率或盈亏比合理
- ✅ 稳定性强，不同时段都有效

重要指标解读：
- 总收益 > 10%
- 夏普 > 1.0
- 最大回撤 < 20%
- 胜率 > 50%
- 盈亏比 > 1.2

---

## ⚠ 重要提醒

不要：
- ✋ 过度优化参数
- ✋ 全仓导入
- ✋ 忽视风控
- ✋ 相信「必赚」扳字

要：
- ✅ 充分回测（2+ 月数据）
- ✅ 从小额开始
- ✅ 严格执行策略规则
- ✅ 运行 1-2 月再评估
- ✅ 设置止损/止盈

---

## 📲 快速命令参考

```bash
streamlit run dashboard.py
python quant_framework.py
# 查看账户信息（待上传模块后使用）
python -c "from binance_futures_example import get_balance; get_balance()"
python binance_trading_strategy.py
```

---

⚠️ 待上传：你本地 `/Users/laok/Documents/GitHub/qlib` 里的已有介绍/使用方法和代码开放后，我会把其中的专有模块和运行流程补充这份文档并做精准排版。
