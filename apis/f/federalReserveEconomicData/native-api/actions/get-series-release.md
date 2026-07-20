# Get Series Release with Federal Reserve Economic Data

Retrieves the release for a series from Federal Reserve Economic Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/fred/series/release`
- **Base URL:** `https://api.stlouisfed.org`
- **Official documentation:** [Get Series Release](https://fred.stlouisfed.org/docs/api/fred/series_release.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `series_id` | query | `string` | yes | The id for a series. |
