# Search Indeed Jobs with ScrapeOps

Retrieves Indeed job search results from ScrapeOps.

## Endpoint

- **Method:** `GET`
- **Path:** `https://proxy.scrapeops.io/v1/structured-data/indeed/job-search`
- **Base URL:** `http://headers.scrapeops.io/v1`
- **Official documentation:** [Search Indeed Jobs](https://scrapeops.io/docs/data-api/indeed-job-search-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location` | query | `string` | no | Location for the Indeed job search. |
| `query` | query | `string` | no | Indeed job search query. |
| `url` | query | `string` | no | Full Indeed jobs search URL to fetch. |
