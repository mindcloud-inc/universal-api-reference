# Financial Modeling Prep: Native API Reference

A consolidated summary of Financial Modeling Prep's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://site.financialmodelingprep.com/developer/docs/quickstart
- **API base URL:** `https://financialmodelingprep.com/stable`

## Authentication

### API Key

Authenticate Financial Modeling Prep requests with your API key. Requests send the key as the shared `apikey` query parameter.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://site.financialmodelingprep.com/developer/docs/quickstart)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–1000). Use `page` in the query string to choose the page; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get As Reported Balance Sheet](actions/get-as-reported-balance-sheet.md) | `GET /balance-sheet-statement-as-reported` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/balance-sheet-statement-as-reported) |
| [Get As Reported Cash Flow Statement](actions/get-as-reported-cash-flow-statement.md) | `GET /cash-flow-statement-as-reported` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/cash-flow-statement-as-reported) |
| [Get As Reported Income Statement](actions/get-as-reported-income-statement.md) | `GET /income-statement-as-reported` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/income-statement-as-reported) |
| [Get Balance Sheet Growth](actions/get-balance-sheet-growth.md) | `GET /balance-sheet-statement-growth` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/balance-sheet-statement-growth) |
| [Get Balance Sheet Statement](actions/get-balance-sheet-statement.md) | `GET /balance-sheet-statement` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/balance-sheet-statement) |
| [Get Cash Flow Growth](actions/get-cash-flow-growth.md) | `GET /cash-flow-statement-growth` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/cash-flow-statement-growth) |
| [Get Cash Flow Statement](actions/get-cash-flow-statement.md) | `GET /cash-flow-statement` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/cash-flow-statement) |
| [Get Company Notes](actions/get-company-notes.md) | `GET /company-notes` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/company-notes) |
| [Get Company Profile](actions/get-company-profile.md) | `GET /profile` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/profile) |
| [Get Dividends](actions/get-dividends.md) | `GET /dividends` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/dividends) |
| [Get Earnings](actions/get-earnings.md) | `GET /earnings` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/earnings) |
| [Get Earnings Calendar](actions/get-earnings-calendar.md) | `GET /earnings-calendar` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/earnings-calendar) |
| [Get Economic Indicators](actions/get-economic-indicators.md) | `GET /economic-indicators` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/economic-indicators) |
| [Get Employee Count](actions/get-employee-count.md) | `GET /employee-count` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/employee-count) |
| [Get Enterprise Values](actions/get-enterprise-values.md) | `GET /enterprise-values` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/enterprise-values) |
| [Get Financial Growth](actions/get-financial-growth.md) | `GET /financial-growth` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/financial-growth) |
| [Get Financial Ratios](actions/get-financial-ratios.md) | `GET /ratios` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/ratios) |
| [Get Financial Ratios TTM](actions/get-financial-ratios-ttm.md) | `GET /ratios-ttm` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/ratios-ttm) |
| [Get Financial Reports Dates](actions/get-financial-reports-dates.md) | `GET /financial-reports-dates` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/financial-reports-dates) |
| [Get Financial Scores](actions/get-financial-scores.md) | `GET /financial-scores` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/financial-scores) |
| [Get Historical Market Capitalization](actions/get-historical-market-capitalization.md) | `GET /historical-market-capitalization` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/historical-market-capitalization) |
| [Get Historical Stock Prices Full](actions/get-historical-stock-prices-full.md) | `GET /historical-price-eod/full` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/historical-price-eod-full) |
| [Get Historical Stock Prices Light](actions/get-historical-stock-prices-light.md) | `GET /historical-price-eod/light` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/historical-price-eod-light) |
| [Get Income Statement](actions/get-income-statement.md) | `GET /income-statement` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/income-statement) |
| [Get Income Statement Growth](actions/get-income-statement-growth.md) | `GET /income-statement-growth` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/income-statement-growth) |
| [Get Key Metrics](actions/get-key-metrics.md) | `GET /key-metrics` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/key-metrics) |
| [Get Key Metrics TTM](actions/get-key-metrics-ttm.md) | `GET /key-metrics-ttm` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/key-metrics-ttm) |
| [Get Market Capitalization](actions/get-market-capitalization.md) | `GET /market-capitalization` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/market-capitalization) |
| [Get Owner Earnings](actions/get-owner-earnings.md) | `GET /owner-earnings` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/owner-earnings) |
| [Get Ratings Snapshot](actions/get-ratings-snapshot.md) | `GET /ratings-snapshot` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/ratings-snapshot) |
| [Get Revenue Geographic Segmentation](actions/get-revenue-geographic-segmentation.md) | `GET /revenue-geographic-segmentation` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/revenue-geographic-segmentation) |
| [Get Revenue Product Segmentation](actions/get-revenue-product-segmentation.md) | `GET /revenue-product-segmentation` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/revenue-product-segmentation) |
| [Get Shares Float](actions/get-shares-float.md) | `GET /shares-float` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/shares-float) |
| [Get Short Stock Quote](actions/get-short-stock-quote.md) | `GET /quote-short` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/quote-short) |
| [Get Stock Peers](actions/get-stock-peers.md) | `GET /stock-peers` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/stock-peers) |
| [Get Stock Quote](actions/get-stock-quote.md) | `GET /quote` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/quote) |
| [Get Stock Splits](actions/get-stock-splits.md) | `GET /splits` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/splits) |
| [Get Treasury Rates](actions/get-treasury-rates.md) | `GET /treasury-rates` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/treasury-rates) |
| [Search Companies By Name](actions/search-companies-by-name.md) | `GET /search-name` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/search-name) |
| [Search Stock Symbols](actions/search-stock-symbols.md) | `GET /search-symbol` | [docs](https://site.financialmodelingprep.com/developer/docs/stable/search-symbol) |
