# AtlasMesh Quant

<p align="center">
  🌐 <strong>Languages:</strong>
  <a href="README.md">English</a> |
  <a href="README.zh.md">中文</a>
</p>

## 🚀 Overview

**AtlasMesh Quant** is an AI-powered quantitative trading system for crypto markets, built on top of Microsoft Qlib.

It bridges research and production:
- 🧠 Qlib for strategy research & modeling
- ⚙️ Execution engine for live trading
- 📊 Dashboard & visualization
- 🧱 Risk management

## ✨ Features

- AI-driven strategy research (Qlib)
- Crypto market support (Binance / OKX / Bybit)
- Backtesting & parameter optimization
- Real-time execution engine
- Web dashboard (Streamlit)

## 🛡️ Architecture
```text
Research (Qlib) -> Signal -> Execution -> Exchange -> Dashboard
```

## ⚡ Quick Start
### 1) Install
```bash
pip install -r requirements.txt
```

### 2) Run framework
```bash
python quant_framework.py
```
This will fetch market data, backtest strategies, optimize parameters, and print performance metrics.

### 3) Launch dashboard
```bash
streamlit run dashboard.py
```
Visit: http://localhost:8501

## 🐎 Strategy Development
```python
class MyStrategy(Strategy):
    def __init__(self):
        super().__init__("My Strategy", "BTCUSDT", "1h")

    def calculate_signal(self, df):
        # your logic
        return signal
```

## 🗂️ Status
🚧 In development

## 📚 Documentation
- [README.zh.md](README.zh.md)
- [docs/workflow.md](docs/workflow.md)
