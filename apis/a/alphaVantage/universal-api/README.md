# <img src="https://images.mindcloud.co/apps/icons/alpha-vantage_1776181921517.png" alt="Alpha Vantage logo" width="28" height="28"> Alpha Vantage: Universal API

Alpha Vantage provides market data, technical indicators, fundamentals, macroeconomic datasets, news sentiment, analytics, and options data through a REST API for equities, ETFs, mutual funds, forex, crypto, commodities, indexes, and macro indicators.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/alphaVantage/latest
- **Actions:** 124
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.alphavantage.co/
- **Vendor API docs:** https://www.alphavantage.co/documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Symbols](actions/search-symbols.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alphaVantage/latest/actions/search-symbols?connectionId=$CONNECTION_ID&keywords=e.g.%20tesco" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (124)

### Adjusted Daily Time Series

| Action | Method | Description |
| --- | --- | --- |
| [Get Adjusted Daily Time Series](actions/get-adjusted-daily-time-series.md) | GET | Retrieves adjusted daily time series data from Alpha Vantage. |

### Adjusted Monthly Time Series

| Action | Method | Description |
| --- | --- | --- |
| [Get Adjusted Monthly Time Series](actions/get-adjusted-monthly-time-series.md) | GET | Retrieves adjusted monthly time series data from Alpha Vantage. |

### Adjusted Weekly Time Series

| Action | Method | Description |
| --- | --- | --- |
| [Get Adjusted Weekly Time Series](actions/get-adjusted-weekly-time-series.md) | GET | Retrieves adjusted weekly time series data from Alpha Vantage. |

### Adosc Indicator

| Action | Method | Description |
| --- | --- | --- |
| [Get ADOSC Indicator](actions/get-adosc-indicator.md) | GET | Retrieves ADOSC indicator data from Alpha Vantage. |

### Adx Indicator

| Action | Method | Description |
| --- | --- | --- |
| [Get ADX Indicator](actions/get-adx-indicator.md) | GET | Retrieves ADX indicator data from Alpha Vantage. |

### Atr Indicator

| Action | Method | Description |
| --- | --- | --- |
| [Get ATR Indicator](actions/get-atr-indicator.md) | GET | Retrieves ATR indicator data from Alpha Vantage. |

### Balance Sheet

| Action | Method | Description |
| --- | --- | --- |
| [Get Balance Sheet](actions/get-balance-sheet.md) | GET | Retrieves balance sheet data from Alpha Vantage. |

### Bbands Indicator

| Action | Method | Description |
| --- | --- | --- |
| [Get BBANDS Indicator](actions/get-bbands-indicator.md) | GET | Retrieves BBANDS indicator data from Alpha Vantage. |

### Brent Oil Prices

| Action | Method | Description |
| --- | --- | --- |
| [Get Brent Oil Prices](actions/get-brent-oil-prices.md) | GET | Retrieves Brent oil price data from Alpha Vantage. |

### Cash Flow

| Action | Method | Description |
| --- | --- | --- |
| [Get Cash Flow](actions/get-cash-flow.md) | GET | Retrieves cash flow data from Alpha Vantage. |

### Catalogs

| Action | Method | Description |
| --- | --- | --- |
| [Get Index Catalog](actions/get-index-catalog.md) | GET | Retrieves the index catalog from Alpha Vantage. |

### Cci Indicator

| Action | Method | Description |
| --- | --- | --- |
| [Get CCI Indicator](actions/get-cci-indicator.md) | GET | Retrieves CCI indicator data from Alpha Vantage. |

### Coffee Prices

| Action | Method | Description |
| --- | --- | --- |
| [Get Coffee Prices](actions/get-coffee-prices.md) | GET | Retrieves coffee price data from Alpha Vantage. |

### Company Overview

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Overview](actions/get-company-overview.md) | GET | Retrieves company overview data from Alpha Vantage. |

### Consumer Price Index

| Action | Method | Description |
| --- | --- | --- |
| [Get CPI](actions/get-cpi.md) | GET | Retrieves CPI data from Alpha Vantage. |

### Copper Prices

| Action | Method | Description |
| --- | --- | --- |
| [Get Copper Prices](actions/get-copper-prices.md) | GET | Retrieves copper price data from Alpha Vantage. |

### Corn Prices

| Action | Method | Description |
| --- | --- | --- |
| [Get Corn Prices](actions/get-corn-prices.md) | GET | Retrieves corn price data from Alpha Vantage. |

### Crypto Daily

| Action | Method | Description |
| --- | --- | --- |
| [Get Crypto Daily](actions/get-crypto-daily.md) | GET | Retrieves crypto daily data from Alpha Vantage. |

### Crypto Intraday

| Action | Method | Description |
| --- | --- | --- |
| [Get Crypto Intraday](actions/get-crypto-intraday.md) | GET | Retrieves crypto intraday data from Alpha Vantage. |

### Crypto Monthly

| Action | Method | Description |
| --- | --- | --- |
| [Get Crypto Monthly](actions/get-crypto-monthly.md) | GET | Retrieves crypto monthly data from Alpha Vantage. |

### Crypto Weekly

| Action | Method | Description |
| --- | --- | --- |
| [Get Crypto Weekly](actions/get-crypto-weekly.md) | GET | Retrieves crypto weekly data from Alpha Vantage. |

### Daily Time Series

| Action | Method | Description |
| --- | --- | --- |
| [Get Daily Time Series](actions/get-daily-time-series.md) | GET | Retrieves daily time series data from Alpha Vantage. |

### Dividends

| Action | Method | Description |
| --- | --- | --- |
| [Get Dividends](actions/get-dividends.md) | GET | Retrieves dividends data from Alpha Vantage. |

### Earnings

| Action | Method | Description |
| --- | --- | --- |
| [Get Earnings](actions/get-earnings.md) | GET | Retrieves earnings data from Alpha Vantage. |

### Earnings Calendar

| Action | Method | Description |
| --- | --- | --- |
| [Get Earnings Calendar](actions/get-earnings-calendar.md) | GET | Retrieves earnings calendar data from Alpha Vantage. |

### Ema Indicator

| Action | Method | Description |
| --- | --- | --- |
| [Get EMA Indicator](actions/get-ema-indicator.md) | GET | Retrieves EMA indicator data from Alpha Vantage. |

### Etf Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get ETF Profile](actions/get-etf-profile.md) | GET | Retrieves ETF profile data from Alpha Vantage. |

### Federal Funds Rate

| Action | Method | Description |
| --- | --- | --- |
| [Get Federal Funds Rate](actions/get-federal-funds-rate.md) | GET | Retrieves federal funds rate data from Alpha Vantage. |

### Forex Daily

| Action | Method | Description |
| --- | --- | --- |
| [Get Forex Daily](actions/get-forex-daily.md) | GET | Retrieves forex daily data from Alpha Vantage. |

### Forex Exchange Rate

| Action | Method | Description |
| --- | --- | --- |
| [Get Forex Exchange Rate](actions/get-forex-exchange-rate.md) | GET | Retrieves forex exchange rate data from Alpha Vantage. |

### Forex Intraday

| Action | Method | Description |
| --- | --- | --- |
| [Get Forex Intraday](actions/get-forex-intraday.md) | GET | Retrieves forex intraday data from Alpha Vantage. |

### Forex Monthly

| Action | Method | Description |
| --- | --- | --- |
| [Get Forex Monthly](actions/get-forex-monthly.md) | GET | Retrieves forex monthly data from Alpha Vantage. |

### Forex Weekly

| Action | Method | Description |
| --- | --- | --- |
| [Get Forex Weekly](actions/get-forex-weekly.md) | GET | Retrieves forex weekly data from Alpha Vantage. |

### Global Quote

| Action | Method | Description |
| --- | --- | --- |
| [Get Global Quote](actions/get-global-quote.md) | GET | Retrieves global quote data from Alpha Vantage. |

### Historical Options

| Action | Method | Description |
| --- | --- | --- |
| [Get Historical Options](actions/get-historical-options.md) | GET | Retrieves historical options data from Alpha Vantage. |

### Income Statement

| Action | Method | Description |
| --- | --- | --- |
| [Get Income Statement](actions/get-income-statement.md) | GET | Retrieves income statement data from Alpha Vantage. |

### Inflation

| Action | Method | Description |
| --- | --- | --- |
| [Get Inflation](actions/get-inflation.md) | GET | Retrieves inflation data from Alpha Vantage. |

### Intraday Time Series

| Action | Method | Description |
| --- | --- | --- |
| [Get Intraday Time Series](actions/get-intraday-time-series.md) | GET | Retrieves intraday time series data from Alpha Vantage. |

### Ipo Calendar

| Action | Method | Description |
| --- | --- | --- |
| [Get IPO Calendar](actions/get-ipo-calendar.md) | GET | Retrieves IPO calendar data from Alpha Vantage. |

### Listing Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Listing Status](actions/get-listing-status.md) | GET | Retrieves listing status data from Alpha Vantage. |

### Macd Indicator

| Action | Method | Description |
| --- | --- | --- |
| [Get MACD Indicator](actions/get-macd-indicator.md) | GET | Retrieves MACD indicator data from Alpha Vantage. |

### Market Movers

| Action | Method | Description |
| --- | --- | --- |
| [List Top Gainers Losers](actions/list-top-gainers-losers.md) | GET | Retrieves top gainers and losers from Alpha Vantage. |

### Market Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Market Status](actions/get-market-status.md) | GET | Retrieves market status data from Alpha Vantage. |

### Mfi Indicator

| Action | Method | Description |
| --- | --- | --- |
| [Get MFI Indicator](actions/get-mfi-indicator.md) | GET | Retrieves MFI indicator data from Alpha Vantage. |

### Monthly Time Series

| Action | Method | Description |
| --- | --- | --- |
| [Get Monthly Time Series](actions/get-monthly-time-series.md) | GET | Retrieves monthly time series data from Alpha Vantage. |

### Natural Gas Prices

| Action | Method | Description |
| --- | --- | --- |
| [Get Natural Gas Prices](actions/get-natural-gas-prices.md) | GET | Retrieves natural gas price data from Alpha Vantage. |

### News Sentiment

| Action | Method | Description |
| --- | --- | --- |
| [Get News Sentiment](actions/get-news-sentiment.md) | GET | Retrieves news sentiment data from Alpha Vantage. |

### Obv Indicator

| Action | Method | Description |
| --- | --- | --- |
| [Get OBV Indicator](actions/get-obv-indicator.md) | GET | Retrieves OBV indicator data from Alpha Vantage. |

### Quotes

| Action | Method | Description |
| --- | --- | --- |
| [Get Realtime Bulk Quotes](actions/get-realtime-bulk-quotes.md) | GET | Retrieves realtime bulk quote data from Alpha Vantage. |

### Real Gdp

| Action | Method | Description |
| --- | --- | --- |
| [Get Real GDP](actions/get-real-gdp.md) | GET | Retrieves real GDP data from Alpha Vantage. |

### Real Gdp Per Capita

| Action | Method | Description |
| --- | --- | --- |
| [Get Real GDP Per Capita](actions/get-real-gdp-per-capita.md) | GET | Retrieves real GDP per capita data from Alpha Vantage. |

### Realtime Options

| Action | Method | Description |
| --- | --- | --- |
| [Get Realtime Options](actions/get-realtime-options.md) | GET | Retrieves realtime options data from Alpha Vantage. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get AD Indicator](actions/get-ad-indicator.md) | GET | Retrieves AD indicator data from Alpha Vantage. |
| [Get ADXR Indicator](actions/get-adxr-indicator.md) | GET | Retrieves ADXR indicator data from Alpha Vantage. |
| [Get All Commodities](actions/get-all-commodities.md) | GET | Retrieves all commodities data from Alpha Vantage. |
| [Get Aluminum Prices](actions/get-aluminum-prices.md) | GET | Retrieves aluminum price data from Alpha Vantage. |
| [Get Analytics Fixed Window](actions/get-analytics-fixed-window.md) | GET | Retrieves analytics fixed window data from Alpha Vantage. |
| [Get Analytics Sliding Window](actions/get-analytics-sliding-window.md) | GET | Retrieves analytics sliding window data from Alpha Vantage. |
| [Get APO Indicator](actions/get-apo-indicator.md) | GET | Retrieves APO indicator data from Alpha Vantage. |
| [Get AROON Indicator](actions/get-aroon-indicator.md) | GET | Retrieves AROON indicator data from Alpha Vantage. |
| [Get AROONOSC Indicator](actions/get-aroonosc-indicator.md) | GET | Retrieves AROONOSC indicator data from Alpha Vantage. |
| [Get BOP Indicator](actions/get-bop-indicator.md) | GET | Retrieves BOP indicator data from Alpha Vantage. |
| [Get CMO Indicator](actions/get-cmo-indicator.md) | GET | Retrieves CMO indicator data from Alpha Vantage. |
| [Get Cotton Prices](actions/get-cotton-prices.md) | GET | Retrieves cotton price data from Alpha Vantage. |
| [Get DEMA Indicator](actions/get-dema-indicator.md) | GET | Retrieves DEMA indicator data from Alpha Vantage. |
| [Get Durables](actions/get-durables.md) | GET | Retrieves durables data from Alpha Vantage. |
| [Get DX Indicator](actions/get-dx-indicator.md) | GET | Retrieves DX indicator data from Alpha Vantage. |
| [Get Earnings Call Transcript](actions/get-earnings-call-transcript.md) | GET | Retrieves an earnings call transcript from Alpha Vantage. |
| [Get Earnings Estimates](actions/get-earnings-estimates.md) | GET | Retrieves earnings estimates data from Alpha Vantage. |
| [Get Gold Silver History](actions/get-gold-silver-history.md) | GET | Retrieves gold and silver price history from Alpha Vantage. |
| [Get Gold Silver Spot](actions/get-gold-silver-spot.md) | GET | Retrieves gold and silver spot prices from Alpha Vantage. |
| [Get Historical Put Call Ratio](actions/get-historical-put-call-ratio.md) | GET | Retrieves historical put call ratio data from Alpha Vantage. |
| [Get Historical Volume Open Interest Ratio](actions/get-historical-volume-open-interest-ratio.md) | GET | Retrieves historical volume open interest ratio data from Alpha Vantage. |
| [Get HT_DCPERIOD Indicator](actions/get-htdcperiod-indicator.md) | GET | Retrieves HT_DCPERIOD indicator data from Alpha Vantage. |
| [Get HT_DCPHASE Indicator](actions/get-htdcphase-indicator.md) | GET | Retrieves HT_DCPHASE indicator data from Alpha Vantage. |
| [Get HT_PHASOR Indicator](actions/get-htphasor-indicator.md) | GET | Retrieves HT_PHASOR indicator data from Alpha Vantage. |
| [Get HT_SINE Indicator](actions/get-htsine-indicator.md) | GET | Retrieves HT_SINE indicator data from Alpha Vantage. |
| [Get HT_TRENDLINE Indicator](actions/get-httrendline-indicator.md) | GET | Retrieves HT_TRENDLINE indicator data from Alpha Vantage. |
| [Get HT_TRENDMODE Indicator](actions/get-httrendmode-indicator.md) | GET | Retrieves HT_TRENDMODE indicator data from Alpha Vantage. |
| [Get Index Data](actions/get-index-data.md) | GET | Retrieves index time series data from Alpha Vantage. |
| [Get Insider Transactions](actions/get-insider-transactions.md) | GET | Retrieves insider transactions data from Alpha Vantage. |
| [Get Institutional Holdings](actions/get-institutional-holdings.md) | GET | Retrieves institutional holdings data from Alpha Vantage. |
| [Get KAMA Indicator](actions/get-kama-indicator.md) | GET | Retrieves KAMA indicator data from Alpha Vantage. |
| [Get MACDEXT Indicator](actions/get-macdext-indicator.md) | GET | Retrieves MACDEXT indicator data from Alpha Vantage. |
| [Get MAMA Indicator](actions/get-mama-indicator.md) | GET | Retrieves MAMA indicator data from Alpha Vantage. |
| [Get MIDPOINT Indicator](actions/get-midpoint-indicator.md) | GET | Retrieves MIDPOINT indicator data from Alpha Vantage. |
| [Get MIDPRICE Indicator](actions/get-midprice-indicator.md) | GET | Retrieves MIDPRICE indicator data from Alpha Vantage. |
| [Get MINUS_DI Indicator](actions/get-minusdi-indicator.md) | GET | Retrieves MINUS_DI indicator data from Alpha Vantage. |
| [Get MINUS_DM Indicator](actions/get-minusdm-indicator.md) | GET | Retrieves MINUS_DM indicator data from Alpha Vantage. |
| [Get MOM Indicator](actions/get-mom-indicator.md) | GET | Retrieves MOM indicator data from Alpha Vantage. |
| [Get NATR Indicator](actions/get-natr-indicator.md) | GET | Retrieves NATR indicator data from Alpha Vantage. |
| [Get Nonfarm Payroll](actions/get-nonfarm-payroll.md) | GET | Retrieves nonfarm payroll data from Alpha Vantage. |
| [Get PLUS_DI Indicator](actions/get-plusdi-indicator.md) | GET | Retrieves PLUS_DI indicator data from Alpha Vantage. |
| [Get PLUS_DM Indicator](actions/get-plusdm-indicator.md) | GET | Retrieves PLUS_DM indicator data from Alpha Vantage. |
| [Get PPO Indicator](actions/get-ppo-indicator.md) | GET | Retrieves PPO indicator data from Alpha Vantage. |
| [Get Realtime Put Call Ratio](actions/get-realtime-put-call-ratio.md) | GET | Retrieves realtime put-call ratio data from Alpha Vantage. |
| [Get Realtime Volume Open Interest Ratio](actions/get-realtime-volume-open-interest-ratio.md) | GET | Retrieves realtime volume open interest ratio data from Alpha Vantage. |
| [Get Retail Sales](actions/get-retail-sales.md) | GET | Retrieves retail sales data from Alpha Vantage. |
| [Get ROC Indicator](actions/get-roc-indicator.md) | GET | Retrieves ROC indicator data from Alpha Vantage. |
| [Get ROCR Indicator](actions/get-rocr-indicator.md) | GET | Retrieves ROCR indicator data from Alpha Vantage. |
| [Get SAR Indicator](actions/get-sar-indicator.md) | GET | Retrieves SAR indicator data from Alpha Vantage. |
| [Get STOCHF Indicator](actions/get-stochf-indicator.md) | GET | Retrieves STOCHF indicator data from Alpha Vantage. |
| [Get Sugar Prices](actions/get-sugar-prices.md) | GET | Retrieves sugar price data from Alpha Vantage. |
| [Get T3 Indicator](actions/get-t3-indicator.md) | GET | Retrieves T3 indicator data from Alpha Vantage. |
| [Get TEMA Indicator](actions/get-tema-indicator.md) | GET | Retrieves TEMA indicator data from Alpha Vantage. |
| [Get TRANGE Indicator](actions/get-trange-indicator.md) | GET | Retrieves TRANGE indicator data from Alpha Vantage. |
| [Get TRIMA Indicator](actions/get-trima-indicator.md) | GET | Retrieves TRIMA indicator data from Alpha Vantage. |
| [Get TRIX Indicator](actions/get-trix-indicator.md) | GET | Retrieves TRIX indicator data from Alpha Vantage. |
| [Get ULTOSC Indicator](actions/get-ultosc-indicator.md) | GET | Retrieves ULTOSC indicator data from Alpha Vantage. |
| [Get Unemployment](actions/get-unemployment.md) | GET | Retrieves unemployment data from Alpha Vantage. |
| [Get VWAP Indicator](actions/get-vwap-indicator.md) | GET | Retrieves VWAP indicator data from Alpha Vantage. |
| [Get Wheat Prices](actions/get-wheat-prices.md) | GET | Retrieves wheat price data from Alpha Vantage. |
| [Get WMA Indicator](actions/get-wma-indicator.md) | GET | Retrieves WMA indicator data from Alpha Vantage. |

### Rsi Indicator

| Action | Method | Description |
| --- | --- | --- |
| [Get RSI Indicator](actions/get-rsi-indicator.md) | GET | Retrieves RSI indicator data from Alpha Vantage. |

### Shares Outstanding

| Action | Method | Description |
| --- | --- | --- |
| [Get Shares Outstanding](actions/get-shares-outstanding.md) | GET | Retrieves shares outstanding data from Alpha Vantage. |

### Sma Indicator

| Action | Method | Description |
| --- | --- | --- |
| [Get SMA Indicator](actions/get-sma-indicator.md) | GET | Retrieves SMA indicator data from Alpha Vantage. |

### Splits

| Action | Method | Description |
| --- | --- | --- |
| [Get Splits](actions/get-splits.md) | GET | Retrieves splits data from Alpha Vantage. |

### Stoch Indicator

| Action | Method | Description |
| --- | --- | --- |
| [Get STOCH Indicator](actions/get-stoch-indicator.md) | GET | Retrieves STOCH indicator data from Alpha Vantage. |

### Stochrsi Indicator

| Action | Method | Description |
| --- | --- | --- |
| [Get STOCHRSI Indicator](actions/get-stochrsi-indicator.md) | GET | Retrieves STOCHRSI indicator data from Alpha Vantage. |

### Symbol Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Symbols](actions/search-symbols.md) | GET | Finds symbols in Alpha Vantage by keywords. |

### Treasury Yield

| Action | Method | Description |
| --- | --- | --- |
| [Get Treasury Yield](actions/get-treasury-yield.md) | GET | Retrieves treasury yield data from Alpha Vantage. |

### Weekly Time Series

| Action | Method | Description |
| --- | --- | --- |
| [Get Weekly Time Series](actions/get-weekly-time-series.md) | GET | Retrieves weekly time series data from Alpha Vantage. |

### Willr Indicator

| Action | Method | Description |
| --- | --- | --- |
| [Get WILLR Indicator](actions/get-willr-indicator.md) | GET | Retrieves WILLR indicator data from Alpha Vantage. |

### Wti Oil Prices

| Action | Method | Description |
| --- | --- | --- |
| [Get WTI Oil Prices](actions/get-wti-oil-prices.md) | GET | Retrieves WTI oil price data from Alpha Vantage. |

