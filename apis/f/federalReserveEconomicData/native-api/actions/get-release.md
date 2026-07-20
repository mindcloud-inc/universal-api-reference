# Get Release with Federal Reserve Economic Data

Retrieves a release from Federal Reserve Economic Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/fred/release`
- **Base URL:** `https://api.stlouisfed.org`
- **Official documentation:** [Get Release](https://fred.stlouisfed.org/docs/api/fred/release.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `release_id` | query | `number` | yes | The id for a release. |
