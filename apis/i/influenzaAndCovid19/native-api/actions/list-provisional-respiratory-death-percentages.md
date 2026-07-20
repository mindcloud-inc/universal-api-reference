# List Provisional Respiratory Death Percentages with Influenza and Covid-19

## Endpoint

- **Method:** `GET`
- **Path:** `/resource/4bc2-bbpq.json`
- **Base URL:** `https://data.cdc.gov`
- **Official documentation:** [List Provisional Respiratory Death Percentages](https://data.cdc.gov/National-Center-for-Health-Statistics/Provisional-Percent-of-Deaths-for-COVID-19-Influen/4bc2-bbpq)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pathogen` | query | `string` | no | Filter to a CDC pathogen value, such as COVID-19, Influenza, or RSV. |
| `week_end` | query | `date` | no | Filter to an exact CDC week ending timestamp, for example 2024-10-05T00:00:00.000. |
| `$where` | query | `string` | no | Optional advanced SoQL where clause for CDC Data.CDC.gov filtering. |
