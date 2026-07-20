# Get daily count of new and lost backlinks with SE Ranking Data

Retrieves daily new and lost backlink counts from SE Ranking Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/backlinks/history/count`
- **Base URL:** `https://api.seranking.com/v1`
- **Official documentation:** [Get daily count of new and lost backlinks](https://seranking.com/api/data/backlinks/#history-count)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target` | query | `string` | yes | Target domain or URL to analyze (for example: seranking.com). |
