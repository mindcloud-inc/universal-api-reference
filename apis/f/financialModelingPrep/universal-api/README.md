# <img src="https://images.mindcloud.co/apps/icons/financial-modeling-prep_1776194231980.png" alt="Financial Modeling Prep logo" width="28" height="28"> Financial Modeling Prep: Universal API

Financial Modeling Prep provides stock market data, company fundamentals, financial statements, market news, calendars, and economic datasets through a stable REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/financialModelingPrep/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://site.financialmodelingprep.com/
- **Vendor API docs:** https://site.financialmodelingprep.com/developer/docs/quickstart

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Stock Symbols](actions/search-stock-symbols.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/financialModelingPrep/latest/actions/search-stock-symbols?connectionId=$CONNECTION_ID&query=AAPL" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### As Reported Balance Sheet

| Action | Method | Description |
| --- | --- | --- |
| [Get As Reported Balance Sheet](actions/get-as-reported-balance-sheet.md) | GET | Retrieves as-reported balance sheet statements from Financial Modeling Prep. |

### As Reported Cash Flow Statement

| Action | Method | Description |
| --- | --- | --- |
| [Get As Reported Cash Flow Statement](actions/get-as-reported-cash-flow-statement.md) | GET | Retrieves as-reported cash flow statements from Financial Modeling Prep. |

### As Reported Income Statement

| Action | Method | Description |
| --- | --- | --- |
| [Get As Reported Income Statement](actions/get-as-reported-income-statement.md) | GET | Retrieves as-reported income statements from Financial Modeling Prep. |

### Balance Sheet Growth

| Action | Method | Description |
| --- | --- | --- |
| [Get Balance Sheet Growth](actions/get-balance-sheet-growth.md) | GET | Retrieves balance sheet growth data from Financial Modeling Prep. |

### Balance Sheet Statement

| Action | Method | Description |
| --- | --- | --- |
| [Get Balance Sheet Statement](actions/get-balance-sheet-statement.md) | GET | Retrieves balance sheet statements from Financial Modeling Prep. |

### Cash Flow Growth

| Action | Method | Description |
| --- | --- | --- |
| [Get Cash Flow Growth](actions/get-cash-flow-growth.md) | GET | Retrieves cash flow growth data from Financial Modeling Prep. |

### Cash Flow Statement

| Action | Method | Description |
| --- | --- | --- |
| [Get Cash Flow Statement](actions/get-cash-flow-statement.md) | GET | Retrieves cash flow statements from Financial Modeling Prep. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Search Companies By Name](actions/search-companies-by-name.md) | GET | Finds companies in Financial Modeling Prep by name. |

### Company Note

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Notes](actions/get-company-notes.md) | GET | Retrieves company notes from Financial Modeling Prep. |

### Company Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Profile](actions/get-company-profile.md) | GET | Retrieves a company profile from Financial Modeling Prep. |

### Dividend

| Action | Method | Description |
| --- | --- | --- |
| [Get Dividends](actions/get-dividends.md) | GET | Retrieves dividends from Financial Modeling Prep. |

### Earnings Calendar Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Earnings Calendar](actions/get-earnings-calendar.md) | GET | Retrieves an earnings calendar from Financial Modeling Prep. |

### Earnings Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Earnings](actions/get-earnings.md) | GET | Retrieves earnings from Financial Modeling Prep. |

### Economic Indicator

| Action | Method | Description |
| --- | --- | --- |
| [Get Economic Indicators](actions/get-economic-indicators.md) | GET | Retrieves economic indicators from Financial Modeling Prep. |

### Employee Count

| Action | Method | Description |
| --- | --- | --- |
| [Get Employee Count](actions/get-employee-count.md) | GET | Retrieves employee count data from Financial Modeling Prep. |

### Enterprise Value

| Action | Method | Description |
| --- | --- | --- |
| [Get Enterprise Values](actions/get-enterprise-values.md) | GET | Retrieves enterprise values from Financial Modeling Prep. |

### Financial Growth

| Action | Method | Description |
| --- | --- | --- |
| [Get Financial Growth](actions/get-financial-growth.md) | GET | Retrieves financial growth data from Financial Modeling Prep. |

### Financial Ratio

| Action | Method | Description |
| --- | --- | --- |
| [Get Financial Ratios](actions/get-financial-ratios.md) | GET | Retrieves financial ratios from Financial Modeling Prep. |

### Financial Ratio Ttm

| Action | Method | Description |
| --- | --- | --- |
| [Get Financial Ratios TTM](actions/get-financial-ratios-ttm.md) | GET | Retrieves trailing twelve-month financial ratios from Financial Modeling Prep. |

### Financial Report Date

| Action | Method | Description |
| --- | --- | --- |
| [Get Financial Reports Dates](actions/get-financial-reports-dates.md) | GET | Retrieves financial report dates from Financial Modeling Prep. |

### Financial Score

| Action | Method | Description |
| --- | --- | --- |
| [Get Financial Scores](actions/get-financial-scores.md) | GET | Retrieves financial scores from Financial Modeling Prep. |

### Historical Market Capitalization

| Action | Method | Description |
| --- | --- | --- |
| [Get Historical Market Capitalization](actions/get-historical-market-capitalization.md) | GET | Retrieves historical market capitalization from Financial Modeling Prep. |

### Historical Stock Price

| Action | Method | Description |
| --- | --- | --- |
| [Get Historical Stock Prices Full](actions/get-historical-stock-prices-full.md) | GET | Retrieves full historical stock prices from Financial Modeling Prep. |
| [Get Historical Stock Prices Light](actions/get-historical-stock-prices-light.md) | GET | Retrieves light historical stock prices from Financial Modeling Prep. |

### Income Statement

| Action | Method | Description |
| --- | --- | --- |
| [Get Income Statement](actions/get-income-statement.md) | GET | Retrieves income statements from Financial Modeling Prep. |

### Income Statement Growth

| Action | Method | Description |
| --- | --- | --- |
| [Get Income Statement Growth](actions/get-income-statement-growth.md) | GET | Retrieves income statement growth data from Financial Modeling Prep. |

### Key Metric

| Action | Method | Description |
| --- | --- | --- |
| [Get Key Metrics](actions/get-key-metrics.md) | GET | Retrieves key metrics from Financial Modeling Prep. |

### Key Metric Ttm

| Action | Method | Description |
| --- | --- | --- |
| [Get Key Metrics TTM](actions/get-key-metrics-ttm.md) | GET | Retrieves trailing twelve-month key metrics from Financial Modeling Prep. |

### Market Capitalization

| Action | Method | Description |
| --- | --- | --- |
| [Get Market Capitalization](actions/get-market-capitalization.md) | GET | Retrieves market capitalization data from Financial Modeling Prep. |

### Owner Earnings

| Action | Method | Description |
| --- | --- | --- |
| [Get Owner Earnings](actions/get-owner-earnings.md) | GET | Retrieves owner earnings from Financial Modeling Prep. |

### Rating Snapshot

| Action | Method | Description |
| --- | --- | --- |
| [Get Ratings Snapshot](actions/get-ratings-snapshot.md) | GET | Retrieves a ratings snapshot from Financial Modeling Prep. |

### Revenue Geographic Segment

| Action | Method | Description |
| --- | --- | --- |
| [Get Revenue Geographic Segmentation](actions/get-revenue-geographic-segmentation.md) | GET | Retrieves revenue segmentation by geography from Financial Modeling Prep. |

### Revenue Product Segment

| Action | Method | Description |
| --- | --- | --- |
| [Get Revenue Product Segmentation](actions/get-revenue-product-segmentation.md) | GET | Retrieves revenue segmentation by product from Financial Modeling Prep. |

### Shares Float

| Action | Method | Description |
| --- | --- | --- |
| [Get Shares Float](actions/get-shares-float.md) | GET | Retrieves shares float data from Financial Modeling Prep. |

### Short Stock Quote

| Action | Method | Description |
| --- | --- | --- |
| [Get Short Stock Quote](actions/get-short-stock-quote.md) | GET | Retrieves a short stock quote from Financial Modeling Prep. |

### Stock Peer

| Action | Method | Description |
| --- | --- | --- |
| [Get Stock Peers](actions/get-stock-peers.md) | GET | Retrieves stock peer companies from Financial Modeling Prep. |

### Stock Quote

| Action | Method | Description |
| --- | --- | --- |
| [Get Stock Quote](actions/get-stock-quote.md) | GET | Retrieves a stock quote from Financial Modeling Prep. |

### Stock Split

| Action | Method | Description |
| --- | --- | --- |
| [Get Stock Splits](actions/get-stock-splits.md) | GET | Retrieves stock splits from Financial Modeling Prep. |

### Stock Symbol

| Action | Method | Description |
| --- | --- | --- |
| [Search Stock Symbols](actions/search-stock-symbols.md) | GET | Finds stock symbols in Financial Modeling Prep by search query. |

### Treasury Rate

| Action | Method | Description |
| --- | --- | --- |
| [Get Treasury Rates](actions/get-treasury-rates.md) | GET | Retrieves treasury rates from Financial Modeling Prep. |

