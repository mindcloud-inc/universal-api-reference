# Get XBRL Frame with United States Securities and Exchange Commission (SEC) EDGAR Database

Retrieves XBRL frame data from SEC EDGAR.

## Endpoint

- **Method:** `GET`
- **Path:** `https://data.sec.gov/api/xbrl/frames/[:taxonomy]/[:tag]/[:unit]/[:period].json`
- **Base URL:** `https://www.sec.gov`
- **Official documentation:** [Get XBRL Frame](https://www.sec.gov/search-filings/edgar-application-programming-interfaces)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taxonomy` | path | `string` | yes | Taxonomy namespace, such as us-gaap, ifrs-full, dei, or srt. |
| `tag` | path | `string` | yes | Taxonomy tag, such as AccountsPayableCurrent. |
| `unit` | path | `string` | yes | XBRL unit, such as USD, shares, pure, or USD-per-shares. |
| `period` | path | `string` | yes | Frame period, such as CY2019, CY2019Q1, or CY2019Q1I. |
