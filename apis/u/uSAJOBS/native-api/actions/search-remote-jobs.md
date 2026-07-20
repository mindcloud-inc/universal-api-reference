# Search Remote Jobs with USAJOBS

Finds remote job postings in USAJOBS.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/Search`
- **Base URL:** `https://data.usajobs.gov`
- **Official documentation:** [Search Remote Jobs](https://developer.usajobs.gov/api-reference/get-api-search)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `RemoteIndicator` | query | `string` | no | True returns only remote jobs; False excludes remote jobs. |
