# Autocomplete Schools with SchoolDigger

Finds school matches in SchoolDigger by partial search text.

## Endpoint

- **Method:** `GET`
- **Path:** `/autocomplete/schools`
- **Base URL:** `https://api.schooldigger.com/v2.3`
- **Official documentation:** [Autocomplete Schools](https://developer.schooldigger.com/llms-full.txt)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `districtID` | query | `string` | no | Optional SchoolDigger district ID filter. |
| `q` | query | `string` | yes | Autocomplete search term. |
| `st` | query | `string` | no | Optional two-letter state code filter. |
| `returnCount` | query | `number` | no | Number of autocomplete matches to return, from 1 to 20. |
| `level` | query | `list` | no | Optional school level filter: Elementary, Middle, High, Alt, or Private. Accepted values: `0`, `1`, `2`, `3`, `4`. |
