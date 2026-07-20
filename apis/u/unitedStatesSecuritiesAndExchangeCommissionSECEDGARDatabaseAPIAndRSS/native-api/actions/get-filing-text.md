# Get Filing Text with United States Securities and Exchange Commission (SEC) EDGAR Database

Retrieves a raw SEC EDGAR filing text file.

## Endpoint

- **Method:** `GET`
- **Path:** `/Archives/edgar/data/[:cik]/[:accessionNumber].txt`
- **Base URL:** `https://www.sec.gov`
- **Official documentation:** [Get Filing Text](https://www.sec.gov/search-filings/edgar-search-assistance/accessing-edgar-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cik` | path | `string` | yes | CIK directory segment, usually without leading zeroes in SEC archive paths. |
| `accessionNumber` | path | `string` | yes | Filing accession number with dashes, such as 0000320193-24-000123. |
