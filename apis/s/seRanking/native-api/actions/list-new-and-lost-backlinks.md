# List new and lost backlinks with SE Ranking Data

Retrieves new and lost backlinks from SE Ranking Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/backlinks/history`
- **Base URL:** `https://api.seranking.com/v1`
- **Official documentation:** [List new and lost backlinks](https://seranking.com/api/data/backlinks/#history)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target` | query | `string` | yes | Target domain or URL to analyze (for example: seranking.com). |
