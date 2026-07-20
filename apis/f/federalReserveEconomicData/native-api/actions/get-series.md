# Get Series with Federal Reserve Economic Data

Retrieves a series from Federal Reserve Economic Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/fred/series`
- **Base URL:** `https://api.stlouisfed.org`
- **Official documentation:** [Get Series](https://fred.stlouisfed.org/docs/api/fred/series.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `series_id` | query | `string` | yes | The id for a series. |
