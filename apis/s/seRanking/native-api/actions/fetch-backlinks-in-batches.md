# Fetch backlinks in batches with SE Ranking Data

Retrieves backlinks in batches from SE Ranking Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/backlinks/raw`
- **Base URL:** `https://api.seranking.com/v1`
- **Official documentation:** [Fetch backlinks in batches](https://seranking.com/api/data/backlinks/#raw)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target` | query | `string` | yes | Target domain or URL to analyze (for example: seranking.com). |
