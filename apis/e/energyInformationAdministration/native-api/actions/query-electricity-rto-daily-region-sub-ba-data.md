# Query Electricity RTO Daily Region Sub BA Data with Energy Information Administration

Retrieves daily RTO region sub-balancing authority data from EIA.

## Endpoint

- **Method:** `GET`
- **Path:** `/electricity/rto/daily-region-sub-ba-data/data`
- **Base URL:** `https://api.eia.gov/v2`
- **Official documentation:** [Query Electricity RTO Daily Region Sub BA Data](https://www.eia.gov/opendata/documentation.php)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[]` | query | `string` | no | One or more EIA data column IDs to return. Send multiple values as a array. |
| `frequency` | query | `string` | no | Optional EIA frequency code for the dataset, such as annual, monthly, daily, or hourly where supported. |
| `start` | query | `string` | no | Optional inclusive start period in the format supported by the selected EIA route. |
| `end` | query | `string` | no | Optional inclusive end period in the format supported by the selected EIA route. |
| `facetFiltersJson` | query | `string` | no | Optional JSON object mapping EIA facet IDs to one or more values. Example: {"stateid":["CA"]}. |
