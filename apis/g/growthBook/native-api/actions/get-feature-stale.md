# Get stale status for one or more features with GrowthBook

Retrieves stale status for GrowthBook features.

## Endpoint

- **Method:** `GET`
- **Path:** `/stale-features`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Get stale status for one or more features](https://docs.growthbook.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | query | `string` | yes | Comma-separated list of feature IDs (URL-encoded if needed). Example: `my_feature,another_feature` |
