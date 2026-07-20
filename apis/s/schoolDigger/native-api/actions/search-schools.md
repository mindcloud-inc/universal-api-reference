# Search Schools with SchoolDigger

Finds schools in SchoolDigger by search criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/schools`
- **Base URL:** `https://api.schooldigger.com/v2.3`
- **Official documentation:** [Search Schools](https://developer.schooldigger.com/llms-full.txt)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `city` | query | `string` | no | Filter schools by city. |
| `districtID` | query | `string` | no | Filter schools to a SchoolDigger district ID. |
| `q` | query | `string` | no | School name or city search term. |
| `st` | query | `string` | yes | Two-letter state code, such as WA or NJ. |
| `zip` | query | `string` | no | Filter schools by five-digit ZIP code. |
| `level` | query | `list` | no | School level filter. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`. |
