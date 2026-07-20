# Alpha Vantage: Native API Reference

A consolidated summary of Alpha Vantage's API configuration and 124 documented operations, with links to official documentation.

- **Official docs:** https://www.alphavantage.co/documentation/
- **API base URL:** `https://www.alphavantage.co`

## Authentication

### Query API Key

Use an Alpha Vantage API key. Runtime requests send the key as the shared `apikey` query parameter using the stored `alphaVantageApiKey` credential field.

### Credentials

- **Alpha Vantage API Key:** `alphaVantageApiKey` · required · Alpha Vantage API key stored in the connection secret payload under `alphaVantageApiKey` and injected into requests as the shared `apikey` query parameter.

[Official authentication documentation](https://www.alphavantage.co/support/#api-key)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (124 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get AD Indicator](actions/get-ad-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Adjusted Daily Time Series](actions/get-adjusted-daily-time-series.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Adjusted Monthly Time Series](actions/get-adjusted-monthly-time-series.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Adjusted Weekly Time Series](actions/get-adjusted-weekly-time-series.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get ADOSC Indicator](actions/get-adosc-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get ADX Indicator](actions/get-adx-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get ADXR Indicator](actions/get-adxr-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get All Commodities](actions/get-all-commodities.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Aluminum Prices](actions/get-aluminum-prices.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Analytics Fixed Window](actions/get-analytics-fixed-window.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Analytics Sliding Window](actions/get-analytics-sliding-window.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get APO Indicator](actions/get-apo-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get AROON Indicator](actions/get-aroon-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get AROONOSC Indicator](actions/get-aroonosc-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get ATR Indicator](actions/get-atr-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Balance Sheet](actions/get-balance-sheet.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get BBANDS Indicator](actions/get-bbands-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get BOP Indicator](actions/get-bop-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Brent Oil Prices](actions/get-brent-oil-prices.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Cash Flow](actions/get-cash-flow.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get CCI Indicator](actions/get-cci-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get CMO Indicator](actions/get-cmo-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Coffee Prices](actions/get-coffee-prices.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Company Overview](actions/get-company-overview.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Copper Prices](actions/get-copper-prices.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Corn Prices](actions/get-corn-prices.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Cotton Prices](actions/get-cotton-prices.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get CPI](actions/get-cpi.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Crypto Daily](actions/get-crypto-daily.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Crypto Intraday](actions/get-crypto-intraday.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Crypto Monthly](actions/get-crypto-monthly.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Crypto Weekly](actions/get-crypto-weekly.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Daily Time Series](actions/get-daily-time-series.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get DEMA Indicator](actions/get-dema-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Dividends](actions/get-dividends.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Durables](actions/get-durables.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get DX Indicator](actions/get-dx-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Earnings](actions/get-earnings.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Earnings Calendar](actions/get-earnings-calendar.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Earnings Call Transcript](actions/get-earnings-call-transcript.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Earnings Estimates](actions/get-earnings-estimates.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get EMA Indicator](actions/get-ema-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get ETF Profile](actions/get-etf-profile.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Federal Funds Rate](actions/get-federal-funds-rate.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Forex Daily](actions/get-forex-daily.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Forex Exchange Rate](actions/get-forex-exchange-rate.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Forex Intraday](actions/get-forex-intraday.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Forex Monthly](actions/get-forex-monthly.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Forex Weekly](actions/get-forex-weekly.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Global Quote](actions/get-global-quote.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Gold Silver History](actions/get-gold-silver-history.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Gold Silver Spot](actions/get-gold-silver-spot.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Historical Options](actions/get-historical-options.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Historical Put Call Ratio](actions/get-historical-put-call-ratio.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Historical Volume Open Interest Ratio](actions/get-historical-volume-open-interest-ratio.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get HT_DCPERIOD Indicator](actions/get-htdcperiod-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get HT_DCPHASE Indicator](actions/get-htdcphase-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get HT_PHASOR Indicator](actions/get-htphasor-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get HT_SINE Indicator](actions/get-htsine-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get HT_TRENDLINE Indicator](actions/get-httrendline-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get HT_TRENDMODE Indicator](actions/get-httrendmode-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Income Statement](actions/get-income-statement.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Index Catalog](actions/get-index-catalog.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Index Data](actions/get-index-data.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Inflation](actions/get-inflation.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Insider Transactions](actions/get-insider-transactions.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Institutional Holdings](actions/get-institutional-holdings.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Intraday Time Series](actions/get-intraday-time-series.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get IPO Calendar](actions/get-ipo-calendar.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get KAMA Indicator](actions/get-kama-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Listing Status](actions/get-listing-status.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get MACD Indicator](actions/get-macd-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get MACDEXT Indicator](actions/get-macdext-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get MAMA Indicator](actions/get-mama-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Market Status](actions/get-market-status.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get MFI Indicator](actions/get-mfi-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get MIDPOINT Indicator](actions/get-midpoint-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get MIDPRICE Indicator](actions/get-midprice-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get MINUS_DI Indicator](actions/get-minusdi-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get MINUS_DM Indicator](actions/get-minusdm-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get MOM Indicator](actions/get-mom-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Monthly Time Series](actions/get-monthly-time-series.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get NATR Indicator](actions/get-natr-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Natural Gas Prices](actions/get-natural-gas-prices.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get News Sentiment](actions/get-news-sentiment.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Nonfarm Payroll](actions/get-nonfarm-payroll.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get OBV Indicator](actions/get-obv-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get PLUS_DI Indicator](actions/get-plusdi-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get PLUS_DM Indicator](actions/get-plusdm-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get PPO Indicator](actions/get-ppo-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Real GDP](actions/get-real-gdp.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Real GDP Per Capita](actions/get-real-gdp-per-capita.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Realtime Bulk Quotes](actions/get-realtime-bulk-quotes.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Realtime Options](actions/get-realtime-options.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Realtime Put Call Ratio](actions/get-realtime-put-call-ratio.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Realtime Volume Open Interest Ratio](actions/get-realtime-volume-open-interest-ratio.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Retail Sales](actions/get-retail-sales.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get ROC Indicator](actions/get-roc-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get ROCR Indicator](actions/get-rocr-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get RSI Indicator](actions/get-rsi-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get SAR Indicator](actions/get-sar-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Shares Outstanding](actions/get-shares-outstanding.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get SMA Indicator](actions/get-sma-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Splits](actions/get-splits.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get STOCH Indicator](actions/get-stoch-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get STOCHF Indicator](actions/get-stochf-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get STOCHRSI Indicator](actions/get-stochrsi-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Sugar Prices](actions/get-sugar-prices.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get T3 Indicator](actions/get-t3-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get TEMA Indicator](actions/get-tema-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get TRANGE Indicator](actions/get-trange-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Treasury Yield](actions/get-treasury-yield.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get TRIMA Indicator](actions/get-trima-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get TRIX Indicator](actions/get-trix-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get ULTOSC Indicator](actions/get-ultosc-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Unemployment](actions/get-unemployment.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get VWAP Indicator](actions/get-vwap-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Weekly Time Series](actions/get-weekly-time-series.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get Wheat Prices](actions/get-wheat-prices.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get WILLR Indicator](actions/get-willr-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get WMA Indicator](actions/get-wma-indicator.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Get WTI Oil Prices](actions/get-wti-oil-prices.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [List Top Gainers Losers](actions/list-top-gainers-losers.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
| [Search Symbols](actions/search-symbols.md) | `GET /query` | [docs](https://www.alphavantage.co/documentation/) |
