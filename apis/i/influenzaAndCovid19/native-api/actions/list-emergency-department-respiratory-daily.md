# List Emergency Department Respiratory Daily with Influenza and Covid-19

## Endpoint

- **Method:** `GET`
- **Path:** `/resource/vjzj-u7u8.json`
- **Base URL:** `https://data.cdc.gov`
- **Official documentation:** [List Emergency Department Respiratory Daily](https://data.cdc.gov/Coronavirus-and-Other-Respiratory-Viruses/NSSP-Emergency-Department-Respiratory-Daily/vjzj-u7u8/about_data)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pathogen` | query | `string` | no | Filter to a CDC pathogen value such as COVID-19, Influenza, RSV, Combined, or ARI. |
| `geography` | query | `string` | no | Filter to a geography value in the CDC dataset, such as United States or a state name. |
| `date` | query | `date` | no | Filter to an exact CDC date timestamp, for example 2022-09-25T00:00:00.000. |
| `$where` | query | `string` | no | Optional advanced SoQL where clause for CDC Data.CDC.gov filtering. |
