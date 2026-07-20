# Download Feed Archive with United States Securities and Exchange Commission (SEC) EDGAR Database

Downloads a daily SEC EDGAR feed archive.

## Endpoint

- **Method:** `GET`
- **Path:** `/Archives/edgar/Feed/[:year]/[:quarter]/[:feedDate].nc.tar.gz`
- **Base URL:** `https://www.sec.gov`
- **Official documentation:** [Download Feed Archive](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | path | `string` | yes | Four-digit year, such as 2026. |
| `quarter` | path | `string` | yes | SEC quarter directory, such as QTR1, QTR2, QTR3, or QTR4. |
| `feedDate` | path | `string` | yes | Feed archive date in YYYYMMDD format. |
