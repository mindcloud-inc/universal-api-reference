# Search Indeed Companies with ScrapeOps

Retrieves Indeed company search results from ScrapeOps.

## Endpoint

- **Method:** `GET`
- **Path:** `https://proxy.scrapeops.io/v1/structured-data/indeed/company-search`
- **Base URL:** `http://headers.scrapeops.io/v1`
- **Official documentation:** [Search Indeed Companies](https://scrapeops.io/docs/data-api/indeed-company-search-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location` | query | `string` | no | Location for the Indeed company search. |
| `query` | query | `string` | no | Indeed company search query. |
| `url` | query | `string` | no | Full Indeed companies search URL to fetch. |
