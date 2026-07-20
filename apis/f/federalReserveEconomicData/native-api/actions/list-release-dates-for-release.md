# List Release Dates For Release with Federal Reserve Economic Data

Retrieves release dates for a release from Federal Reserve Economic Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/fred/release/dates`
- **Base URL:** `https://api.stlouisfed.org`
- **Official documentation:** [List Release Dates For Release](https://fred.stlouisfed.org/docs/api/fred/release_dates.html)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_release_dates_with_no_data` | query | `boolean` | no | Return release dates even when no data is available for them. |
| `release_id` | query | `number` | yes | The id for a release. |
