# Get Company Submissions File with United States Securities and Exchange Commission (SEC) EDGAR Database

Retrieves a company submissions file from SEC EDGAR.

## Endpoint

- **Method:** `GET`
- **Path:** `https://data.sec.gov/submissions/[:fileName]`
- **Base URL:** `https://www.sec.gov`
- **Official documentation:** [Get Company Submissions File](https://www.sec.gov/search-filings/edgar-application-programming-interfaces)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileName` | path | `string` | yes | Submissions file name returned in filings.files, such as CIK0000320193-submissions-001.json. |
