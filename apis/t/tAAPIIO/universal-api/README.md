# <img src="https://images.mindcloud.co/apps/icons/t-aapiio_1775875568101.png" alt="TAAPI.IO logo" width="28" height="28"> TAAPI.IO: Universal API

TAAPI.IO provides read-only REST endpoints for real-time and historical technical indicator calculations across crypto, stocks, and ETFs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tAAPIIO/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://taapi.io
- **Vendor API docs:** https://taapi.io/documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get RSI](actions/get-rsi.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tAAPIIO/latest/actions/get-rsi?connectionId=$CONNECTION_ID&exchange=binance&symbol=BTC%2FUSDT&interval=1h" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Datasets

| Action | Method | Description |
| --- | --- | --- |
| [Get Accelerator Oscillator](actions/get-accelerator-oscillator.md) | GET | Retrieves Accelerator Oscillator indicator data from TAAPI.IO. |
| [Get Aroon](actions/get-aroon.md) | GET | Retrieves Aroon indicator data from TAAPI.IO. |
| [Get Average True Range](actions/get-atr.md) | GET | Retrieves Average True Range indicator data from TAAPI.IO. |
| [Get Average Directional Movement Index](actions/get-average-directional-movement-index.md) | GET | Retrieves Average Directional Movement Index data from TAAPI.IO. |
| [Get Average Directional Movement Index Rating](actions/get-average-directional-movement-index-rating.md) | GET | Retrieves Average Directional Movement Index Rating data from TAAPI.IO. |
| [Get Awesome Oscillator](actions/get-awesome-oscillator.md) | GET | Retrieves Awesome Oscillator indicator data from TAAPI.IO. |
| [Get Bollinger Bands](actions/get-bbands.md) | GET | Retrieves Bollinger Bands indicator data from TAAPI.IO. |
| [Get Commodity Channel Index](actions/get-cci.md) | GET | Retrieves Commodity Channel Index indicator data from TAAPI.IO. |
| [Get Chaikin Money Flow](actions/get-cmf.md) | GET | Retrieves Chaikin Money Flow indicator data from TAAPI.IO. |
| [Get Directional Movement Index](actions/get-dmi.md) | GET | Retrieves Directional Movement Index indicator data from TAAPI.IO. |
| [Get Exponential Moving Average](actions/get-ema.md) | GET | Retrieves Exponential Moving Average indicator data from TAAPI.IO. |
| [Get Hull Moving Average](actions/get-hma.md) | GET | Retrieves Hull Moving Average indicator data from TAAPI.IO. |
| [Get Ichimoku Cloud](actions/get-ichimoku.md) | GET | Retrieves Ichimoku Cloud indicator data from TAAPI.IO. |
| [Get Moving Average](actions/get-ma.md) | GET | Retrieves Moving Average indicator data from TAAPI.IO. |
| [Get MACD](actions/get-macd.md) | GET | Retrieves MACD indicator data from TAAPI.IO. |
| [Get Money Flow Index](actions/get-mfi.md) | GET | Retrieves Money Flow Index indicator data from TAAPI.IO. |
| [Get Momentum](actions/get-mom.md) | GET | Retrieves Momentum indicator data from TAAPI.IO. |
| [Get Pivot Points](actions/get-pivot-points.md) | GET | Retrieves Pivot Points indicator data from TAAPI.IO. |
| [Get Parabolic SAR](actions/get-psar.md) | GET | Retrieves Parabolic SAR indicator data from TAAPI.IO. |
| [Get Rate of Change](actions/get-roc.md) | GET | Retrieves Rate of Change indicator data from TAAPI.IO. |
| [Get RSI](actions/get-rsi.md) | GET | Retrieves RSI indicator data from TAAPI.IO. |
| [Get Standard Deviation](actions/get-stddev.md) | GET | Retrieves Standard Deviation indicator data from TAAPI.IO. |
| [Get Stochastic](actions/get-stoch.md) | GET | Retrieves Stochastic indicator data from TAAPI.IO. |
| [Get StochRSI](actions/get-stoch-rsi.md) | GET | Retrieves StochRSI indicator data from TAAPI.IO. |
| [Get Supertrend](actions/get-supertrend.md) | GET | Retrieves Supertrend indicator data from TAAPI.IO. |
| [Get TRIX](actions/get-trix.md) | GET | Retrieves TRIX indicator data from TAAPI.IO. |
| [Get Ultimate Oscillator](actions/get-ultosc.md) | GET | Retrieves Ultimate Oscillator indicator data from TAAPI.IO. |
| [Get VWAP](actions/get-vwap.md) | GET | Retrieves VWAP indicator data from TAAPI.IO. |
| [Get Williams %R](actions/get-williams-r.md) | GET | Retrieves Williams %R indicator data from TAAPI.IO. |

### Prices

| Action | Method | Description |
| --- | --- | --- |
| [Get Candles](actions/get-candles.md) | GET | Retrieves candlestick data for a market from TAAPI.IO. |

