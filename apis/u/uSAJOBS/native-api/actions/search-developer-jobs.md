# Search Developer Jobs with USAJOBS

Finds developer job postings in USAJOBS.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/Search`
- **Base URL:** `https://data.usajobs.gov`
- **Official documentation:** [Search Developer Jobs](https://developer.usajobs.gov/api-reference/get-api-search)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Keyword` | query | `string` | no | Search term used to find matching job announcements. |
