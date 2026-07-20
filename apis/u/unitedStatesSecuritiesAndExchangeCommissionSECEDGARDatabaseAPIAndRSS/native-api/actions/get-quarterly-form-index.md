# Get Quarterly Form Index with United States Securities and Exchange Commission (SEC) EDGAR Database

Retrieves the SEC EDGAR quarterly form index file.

## Endpoint

- **Method:** `GET`
- **Path:** `/Archives/edgar/full-index/[:year]/[:quarter]/form.idx`
- **Base URL:** `https://www.sec.gov`
- **Official documentation:** [Get Quarterly Form Index](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | path | `string` | no | Four-digit year, such as 2026. |
| `year` | path | `string` | yes | Four-digit year, such as 2026. |
| `quarter` | path | `string` | yes | SEC quarter directory, such as QTR1, QTR2, QTR3, or QTR4. |
