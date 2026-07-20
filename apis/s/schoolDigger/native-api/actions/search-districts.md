# Search Districts with SchoolDigger

Finds districts in SchoolDigger by search criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/districts`
- **Base URL:** `https://api.schooldigger.com/v2.3`
- **Official documentation:** [Search Districts](https://developer.schooldigger.com/llms-full.txt)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `city` | query | `string` | no | Filter districts by city. |
| `q` | query | `string` | no | District name or city search term. |
| `st` | query | `string` | yes | Two-letter state code, such as WA or NJ. |
| `zip` | query | `string` | no | Filter districts by five-digit ZIP code. |
