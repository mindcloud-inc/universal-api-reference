# Get Daily XBRL Index with United States Securities and Exchange Commission (SEC) EDGAR Database

Retrieves the SEC EDGAR daily XBRL index file.

## Endpoint

- **Method:** `GET`
- **Path:** `/Archives/edgar/daily-index/xbrl/[:year]/[:quarter]/xbrl.[:date].idx`
- **Base URL:** `https://www.sec.gov`
- **Official documentation:** [Get Daily XBRL Index](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | path | `string` | yes | Four-digit year, such as 2026. |
| `quarter` | path | `string` | yes | SEC quarter directory, such as QTR1, QTR2, QTR3, or QTR4. |
| `date` | path | `string` | yes | Daily index file date in YYYYMMDD format. |
