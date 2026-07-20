# List Browser Headers with ScrapeOps

Retrieves fake browser headers from ScrapeOps.

## Endpoint

- **Method:** `GET`
- **Path:** `/browser-headers`
- **Base URL:** `http://headers.scrapeops.io/v1`
- **Official documentation:** [List Browser Headers](https://scrapeops.io/docs/fake-user-agent-headers-api/fake-browser-headers/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `num_results` | query | `number` | no | How many browser headers to return |
| `mobile` | query | `boolean` | no | Return mobile browser headers only when true |
