# Get Company Concept with United States Securities and Exchange Commission (SEC) EDGAR Database

Retrieves company concept facts from SEC EDGAR.

## Endpoint

- **Method:** `GET`
- **Path:** `https://data.sec.gov/api/xbrl/companyconcept/CIK[:cik]/[:taxonomy]/[:tag].json`
- **Base URL:** `https://www.sec.gov`
- **Official documentation:** [Get Company Concept](https://www.sec.gov/search-filings/edgar-application-programming-interfaces)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cik` | path | `string` | yes | Zero-padded 10-digit Central Index Key. |
| `taxonomy` | path | `string` | yes | Taxonomy namespace, such as us-gaap, ifrs-full, dei, or srt. |
| `tag` | path | `string` | yes | Taxonomy tag, such as AccountsPayableCurrent. |
