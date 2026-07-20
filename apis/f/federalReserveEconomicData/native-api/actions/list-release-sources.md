# List Release Sources with Federal Reserve Economic Data

Retrieves sources for a release from Federal Reserve Economic Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/fred/release/sources`
- **Base URL:** `https://api.stlouisfed.org`
- **Official documentation:** [List Release Sources](https://fred.stlouisfed.org/docs/api/fred/release_sources.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `release_id` | query | `number` | yes | The id for a release. |
