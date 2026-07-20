# Get backlink summary with SE Ranking Data

Retrieves a backlink summary from SE Ranking Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/backlinks/summary`
- **Base URL:** `https://api.seranking.com/v1`
- **Official documentation:** [Get backlink summary](https://seranking.com/api/data/backlinks/#summary)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mode` | query | `string` | no | Target type: domain, subdomain, URL, or exact URL. |
| `target` | query | `string` | yes | Target domain or URL to analyze (for example: seranking.com). |
