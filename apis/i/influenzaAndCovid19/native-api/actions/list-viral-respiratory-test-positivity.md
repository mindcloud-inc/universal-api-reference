# List Viral Respiratory Test Positivity with Influenza and Covid-19

## Endpoint

- **Method:** `GET`
- **Path:** `/resource/seuz-s2cv.json`
- **Base URL:** `https://data.cdc.gov`
- **Official documentation:** [List Viral Respiratory Test Positivity](https://data.cdc.gov/Public-Health-Surveillance/Percent-of-Tests-Positive-for-Viral-Respiratory-Pa/seuz-s2cv)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pathogen` | query | `string` | no | Filter to a CDC pathogen value, such as COVID-19, Influenza, or RSV. |
| `week_end` | query | `date` | no | Filter to an exact CDC week ending timestamp, for example 2022-10-01T00:00:00.000. |
| `$where` | query | `string` | no | Optional advanced SoQL where clause for CDC Data.CDC.gov filtering. |
