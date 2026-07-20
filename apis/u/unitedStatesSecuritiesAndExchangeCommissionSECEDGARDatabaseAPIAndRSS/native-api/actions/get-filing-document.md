# Get Filing Document with United States Securities and Exchange Commission (SEC) EDGAR Database

Retrieves a filing document from the SEC EDGAR archive.

## Endpoint

- **Method:** `GET`
- **Path:** `/Archives/edgar/data/[:cik]/[:accessionNumberNoDashes]/[:documentName]`
- **Base URL:** `https://www.sec.gov`
- **Official documentation:** [Get Filing Document](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cik` | path | `string` | yes | CIK directory segment, usually without leading zeroes in SEC archive paths. |
| `accessionNumberNoDashes` | path | `string` | yes | Accession number directory segment without dashes. |
| `documentName` | path | `string` | yes | Document file name inside the filing directory, such as aapl-20240928.htm. |
