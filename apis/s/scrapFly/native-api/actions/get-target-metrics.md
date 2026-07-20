# Get Target Metrics with ScrapFly

Retrieves target monitoring metrics from ScrapFly.

## Endpoint

- **Method:** `GET`
- **Path:** `/scrape/monitoring/metrics/target`
- **Base URL:** `https://api.scrapfly.io`
- **Official documentation:** [Get Target Metrics](https://scrapfly.io/docs/monitoring)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | yes | Target domain to retrieve monitoring metrics for. |
