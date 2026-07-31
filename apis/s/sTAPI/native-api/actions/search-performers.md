# Search Performers with STAPI

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/rest/performer/search`
- **Base URL:** `https://stapi.co/api`
- **Official documentation:** [Search Performers](https://stapi.co/api-documentation)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Performer name |
