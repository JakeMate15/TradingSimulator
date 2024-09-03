# TradingSimulator

### Constraints
- **Minimum order gap per symbol**: 10 seconds.
- **Max Net Open Positions (NOP)**: $10 million.

### Build Command
```bash
g++ -O3 -std=c++20 -o sim.exe internal/*.cpp sample_<my_strategy.cpp>
```

## Trading Platform API Overview

### EventDispatcher
- Main abstraction of an event loop.
- Handles tasks like scheduling and executing events in order.

### Market Data (TopOfBook)
- Provides real-time data on bid and ask prices and sizes.

### Order Handling
- Interfaces and classes for managing buy/sell orders, including callbacks for updates.

### Strategy Interface
- Framework for implementing trading strategies using the API.

---

## Example Strategies

### Flipper
- **Description**: Alternates between buy and sell orders every minute.

### Spread-based Trader (Gambler)
- **Description**: Trades based on the spread between bid and ask prices, entering positions when conditions are favorable.

---

## Risk Interface

- **Purpose**: Measure and manage risks, and evaluate performance via Profit and Loss (PnL).
- **Key Functions**: `getPnL`, `getNOP` to calculate total PnL and aggregate positions.

---

## Disclaimer

It is intended solely for informational purposes and should not be construed as investment advice.
