# List Series Observations with Federal Reserve Economic Data

Retrieves series observations from Federal Reserve Economic Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/fred/series/observations`
- **Base URL:** `https://api.stlouisfed.org`
- **Official documentation:** [List Series Observations](https://fred.stlouisfed.org/docs/api/fred/series_observations.html)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `aggregation_method` | query | `string` | no | The aggregation method used for frequency aggregation. |
| `frequency` | query | `string` | no | Aggregate values to a lower frequency. |
| `observation_end` | query | `date` | no | The end of the observation period. |
| `observation_start` | query | `date` | no | The start of the observation period. |
| `output_type` | query | `number` | no | An integer that indicates an output type. |
| `series_id` | query | `string` | yes | The id for a series. |
| `units` | query | `string` | no | A key that indicates a data value transformation. |
| `vintage_dates` | query | `string` | no | A comma separated list of vintage dates in YYYY-MM-DD format. |
