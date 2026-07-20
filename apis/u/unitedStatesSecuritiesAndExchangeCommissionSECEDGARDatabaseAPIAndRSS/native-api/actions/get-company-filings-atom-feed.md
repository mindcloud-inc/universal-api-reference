# Get Company Filings Atom Feed with United States Securities and Exchange Commission (SEC) EDGAR Database

Retrieves a company filings Atom feed from SEC EDGAR.

## Endpoint

- **Method:** `GET`
- **Path:** `/cgi-bin/browse-edgar`
- **Base URL:** `https://www.sec.gov`
- **Official documentation:** [Get Company Filings Atom Feed](https://www.sec.gov/about/rss-feeds)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CIK` | query | `string` | yes | Company CIK or ticker symbol. |
| `type` | query | `string` | no | Optional SEC form type filter, such as 10-K, 10-Q, or 8-K. |
| `owner` | query | `string` | no | Ownership filing mode, such as exclude or include. |
| `count` | query | `number` | no | Maximum number of feed entries returned by SEC browse search. |
