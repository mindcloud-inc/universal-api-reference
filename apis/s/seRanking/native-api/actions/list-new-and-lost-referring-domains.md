# List new and lost referring domains with SE Ranking Data

Retrieves new and lost referring domains from SE Ranking Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/backlinks/refdomains/history`
- **Base URL:** `https://api.seranking.com/v1`
- **Official documentation:** [List new and lost referring domains](https://seranking.com/api/data/backlinks/#refdomains-history)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target` | query | `string` | yes | Target domain or URL to analyze (for example: seranking.com). |
