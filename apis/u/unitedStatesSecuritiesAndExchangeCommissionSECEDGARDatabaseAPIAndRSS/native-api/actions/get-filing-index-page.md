# Get Filing Index Page with United States Securities and Exchange Commission (SEC) EDGAR Database

Retrieves a filing index page from SEC EDGAR.

## Endpoint

- **Method:** `GET`
- **Path:** `/Archives/edgar/data/[:cik]/[:accessionNumberNoDashes]/[:accessionNumber]-index.html`
- **Base URL:** `https://www.sec.gov`
- **Official documentation:** [Get Filing Index Page](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cik` | path | `string` | yes | CIK directory segment, usually without leading zeroes in SEC archive paths. |
| `accessionNumberNoDashes` | path | `string` | yes | Accession number directory segment without dashes. |
| `accessionNumber` | path | `string` | yes | Filing accession number with dashes, such as 0000320193-24-000123. |
