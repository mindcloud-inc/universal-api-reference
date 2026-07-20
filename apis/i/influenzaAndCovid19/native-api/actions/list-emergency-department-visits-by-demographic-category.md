# List Emergency Department Visits by Demographic Category with Influenza and Covid-19

## Endpoint

- **Method:** `GET`
- **Path:** `/resource/7xva-uux8.json`
- **Base URL:** `https://data.cdc.gov`
- **Official documentation:** [List Emergency Department Visits by Demographic Category](https://data.cdc.gov/Public-Health-Surveillance/NSSP-Emergency-Department-Visits-COVID-19-Flu-RSV-/7xva-uux8)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pathogen` | query | `string` | no | Filter to a CDC pathogen value such as COVID-19, Influenza, RSV, Combined, or ARI. |
| `geography` | query | `string` | no | Filter to a geography value in the CDC dataset, such as United States or a state name. |
| `demographics_type` | query | `string` | no | Filter to the demographic category type reported by CDC, such as Age Group or Sex. |
| `demographics_values` | query | `string` | no | Filter to a specific demographic value reported by CDC, such as 50-64 years. |
| `week_end` | query | `date` | no | Filter to an exact CDC week ending timestamp, for example 2026-04-18T00:00:00.000. |
| `$where` | query | `string` | no | Optional advanced SoQL where clause for CDC Data.CDC.gov filtering when exact-match fields are not enough. |
