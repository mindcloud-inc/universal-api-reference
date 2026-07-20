# Get daily count of new and lost referring domains with SE Ranking Data

Retrieves daily new and lost referring domain counts from SE Ranking Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/backlinks/refdomains/history/count`
- **Base URL:** `https://api.seranking.com/v1`
- **Official documentation:** [Get daily count of new and lost referring domains](https://seranking.com/api/data/backlinks/#refdomains-history-count)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target` | query | `string` | yes | Target domain or URL to analyze (for example: seranking.com). |
