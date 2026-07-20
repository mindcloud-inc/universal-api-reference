# Get Source with Federal Reserve Economic Data

Retrieves a source from Federal Reserve Economic Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/fred/source`
- **Base URL:** `https://api.stlouisfed.org`
- **Official documentation:** [Get Source](https://fred.stlouisfed.org/docs/api/fred/source.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source_id` | query | `number` | yes | The id for a source. |
