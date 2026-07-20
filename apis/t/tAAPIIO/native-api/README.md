# TAAPI.IO: Native API Reference

A consolidated summary of TAAPI.IO's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://taapi.io/documentation/
- **API base URL:** `https://api.taapi.io`

## Authentication

### API Key

Use the TAAPI.IO secret that is emailed to you after you request API access.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://taapi.io/documentation/get-started/)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Accelerator Oscillator](actions/get-accelerator-oscillator.md) | `GET /accosc` | [docs](https://taapi.io/indicators/accelerator-oscillator/) |
| [Get Aroon](actions/get-aroon.md) | `GET /aroon` | [docs](https://taapi.io/indicators/aroon/) |
| [Get Average True Range](actions/get-atr.md) | `GET /atr` | [docs](https://taapi.io/indicators/average-true-range/) |
| [Get Average Directional Movement Index](actions/get-average-directional-movement-index.md) | `GET /adx` | [docs](https://taapi.io/indicators/adx/) |
| [Get Average Directional Movement Index Rating](actions/get-average-directional-movement-index-rating.md) | `GET /adxr` | [docs](https://taapi.io/indicators/average-directional-movement-index-rating/) |
| [Get Awesome Oscillator](actions/get-awesome-oscillator.md) | `GET /ao` | [docs](https://taapi.io/indicators/awesome-oscillator/) |
| [Get Bollinger Bands](actions/get-bbands.md) | `GET /bbands` | [docs](https://taapi.io/indicators/bollinger-bands/) |
| [Get Candles](actions/get-candles.md) | `GET /candles` | [docs](https://taapi.io/indicators/candles/) |
| [Get Commodity Channel Index](actions/get-cci.md) | `GET /cci` | [docs](https://taapi.io/indicators/commodity-channel-index/) |
| [Get Chaikin Money Flow](actions/get-cmf.md) | `GET /cmf` | [docs](https://taapi.io/indicators/chaikin-money-flow/) |
| [Get Directional Movement Index](actions/get-dmi.md) | `GET /dmi` | [docs](https://taapi.io/indicators/directional-movement-index/) |
| [Get Exponential Moving Average](actions/get-ema.md) | `GET /ema` | [docs](https://taapi.io/indicators/exponential-moving-average/) |
| [Get Hull Moving Average](actions/get-hma.md) | `GET /hma` | [docs](https://taapi.io/indicators/hull-moving-average/) |
| [Get Ichimoku Cloud](actions/get-ichimoku.md) | `GET /ichimoku` | [docs](https://taapi.io/indicators/ichimoku-cloud/) |
| [Get Moving Average](actions/get-ma.md) | `GET /ma` | [docs](https://taapi.io/indicators/moving-average/) |
| [Get MACD](actions/get-macd.md) | `GET /macd` | [docs](https://taapi.io/indicators/macd/) |
| [Get Money Flow Index](actions/get-mfi.md) | `GET /mfi` | [docs](https://taapi.io/indicators/money-flow-index/) |
| [Get Momentum](actions/get-mom.md) | `GET /mom` | [docs](https://taapi.io/indicators/momentum/) |
| [Get Pivot Points](actions/get-pivot-points.md) | `GET /pivotpoints` | [docs](https://taapi.io/indicators/pivot-points/) |
| [Get Parabolic SAR](actions/get-psar.md) | `GET /psar` | [docs](https://taapi.io/indicators/parabolic-sar/) |
| [Get Rate of Change](actions/get-roc.md) | `GET /roc` | [docs](https://taapi.io/indicators/rate-of-change/) |
| [Get RSI](actions/get-rsi.md) | `GET /rsi` | [docs](https://taapi.io/indicators/relative-strength-index-rsi/) |
| [Get Standard Deviation](actions/get-stddev.md) | `GET /stddev` | [docs](https://taapi.io/indicators/standard-deviation/) |
| [Get Stochastic](actions/get-stoch.md) | `GET /stoch` | [docs](https://taapi.io/indicators/stochastic/) |
| [Get StochRSI](actions/get-stoch-rsi.md) | `GET /stochrsi` | [docs](https://taapi.io/indicators/stochrsi-stochastic-relative-strength-index/) |
| [Get Supertrend](actions/get-supertrend.md) | `GET /supertrend` | [docs](https://taapi.io/indicators/supertrend/) |
| [Get TRIX](actions/get-trix.md) | `GET /trix` | [docs](https://taapi.io/indicators/trix/) |
| [Get Ultimate Oscillator](actions/get-ultosc.md) | `GET /ultosc` | [docs](https://taapi.io/indicators/ultimate-oscillator/) |
| [Get VWAP](actions/get-vwap.md) | `GET /vwap` | [docs](https://taapi.io/indicators/volume-weighted-average-price-vwap/) |
| [Get Williams %R](actions/get-williams-r.md) | `GET /willr` | [docs](https://taapi.io/indicators/williams-r/) |
