# Get Structured Disclosure Monthly RSS Archive with United States Securities and Exchange Commission (SEC) EDGAR Database

Retrieves a monthly structured disclosure RSS archive from SEC EDGAR.

## Endpoint

- **Method:** `GET`
- **Path:** `/Archives/edgar/monthly/xbrlrss-[:yearMonth].xml`
- **Base URL:** `https://www.sec.gov`
- **Official documentation:** [Get Structured Disclosure Monthly RSS Archive](https://www.sec.gov/data-research/structured-data/structured-disclosure-rss-feeds)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `yearMonth` | path | `string` | yes | Structured disclosure monthly archive identifier in YYYY-MM format. |
