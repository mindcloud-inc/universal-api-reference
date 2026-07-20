# Get Company Submissions with United States Securities and Exchange Commission (SEC) EDGAR Database

Retrieves company submission history from SEC EDGAR.

## Endpoint

- **Method:** `GET`
- **Path:** `https://data.sec.gov/submissions/CIK[:cik].json`
- **Base URL:** `https://www.sec.gov`
- **Official documentation:** [Get Company Submissions](https://www.sec.gov/search-filings/edgar-application-programming-interfaces)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cik` | path | `string` | yes | Zero-padded 10-digit Central Index Key, such as 0000320193 for Apple. |
