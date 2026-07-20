# Autocomplete Districts with SchoolDigger

Finds district matches in SchoolDigger by partial search text.

## Endpoint

- **Method:** `GET`
- **Path:** `/autocomplete/districts`
- **Base URL:** `https://api.schooldigger.com/v2.3`
- **Official documentation:** [Autocomplete Districts](https://developer.schooldigger.com/llms-full.txt)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Autocomplete search term. |
| `st` | query | `string` | no | Optional two-letter state code filter. |
| `returnCount` | query | `number` | no | Number of autocomplete matches to return, from 1 to 20. |
