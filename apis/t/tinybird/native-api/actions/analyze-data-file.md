# Analyze Data File with Tinybird

## Endpoint

- **Method:** `POST`
- **Path:** `v0/analyze`
- **Base URL:** `{apiHost}`
- **Official documentation:** [Analyze Data File](https://www.tinybird.co/docs/api-reference/analyze-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | Remote CSV, NDJSON, or Parquet file URL to analyze |
