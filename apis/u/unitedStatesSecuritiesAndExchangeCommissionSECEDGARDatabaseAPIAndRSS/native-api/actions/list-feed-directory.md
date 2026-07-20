# List Feed Directory with United States Securities and Exchange Commission (SEC) EDGAR Database

Retrieves the SEC EDGAR quarterly feed directory listing.

## Endpoint

- **Method:** `GET`
- **Path:** `/Archives/edgar/Feed/[:year]/[:quarter]/index.json`
- **Base URL:** `https://www.sec.gov`
- **Official documentation:** [List Feed Directory](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | path | `string` | yes | Four-digit year, such as 2026. |
| `quarter` | path | `string` | yes | SEC quarter directory, such as QTR1, QTR2, QTR3, or QTR4. |
