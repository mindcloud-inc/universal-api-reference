# List Release Series with Federal Reserve Economic Data

Retrieves series for a release from Federal Reserve Economic Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/fred/release/series`
- **Base URL:** `https://api.stlouisfed.org`
- **Official documentation:** [List Release Series](https://fred.stlouisfed.org/docs/api/fred/release_series.html)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `release_id` | query | `number` | yes | The id for a release. |
