# List Source Releases with Federal Reserve Economic Data

Retrieves releases for a source from Federal Reserve Economic Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/fred/source/releases`
- **Base URL:** `https://api.stlouisfed.org`
- **Official documentation:** [List Source Releases](https://fred.stlouisfed.org/docs/api/fred/source_releases.html)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source_id` | query | `number` | yes | The id for a source. |
