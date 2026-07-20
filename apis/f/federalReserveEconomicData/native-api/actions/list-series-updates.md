# List Series Updates with Federal Reserve Economic Data

Retrieves series updates from Federal Reserve Economic Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/fred/series/updates`
- **Base URL:** `https://api.stlouisfed.org`
- **Official documentation:** [List Series Updates](https://fred.stlouisfed.org/docs/api/fred/series_updates.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end_time` | query | `string` | no | End time for limiting results for a time range, formatted as YYYYMMDDHhmm. |
| `filter_value` | query | `string` | no | Limit results by geographic type of economic data series. |
| `start_time` | query | `string` | no | Start time for limiting results for a time range, formatted as YYYYMMDDHhmm. |
