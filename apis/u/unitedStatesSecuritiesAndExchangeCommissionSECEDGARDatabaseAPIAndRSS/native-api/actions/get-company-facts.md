# Get Company Facts with United States Securities and Exchange Commission (SEC) EDGAR Database

Retrieves company XBRL facts from SEC EDGAR.

## Endpoint

- **Method:** `GET`
- **Path:** `https://data.sec.gov/api/xbrl/companyfacts/CIK[:cik].json`
- **Base URL:** `https://www.sec.gov`
- **Official documentation:** [Get Company Facts](https://www.sec.gov/search-filings/edgar-application-programming-interfaces)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cik` | path | `string` | yes | Zero-padded 10-digit Central Index Key, such as 0000320193 for Apple. |
