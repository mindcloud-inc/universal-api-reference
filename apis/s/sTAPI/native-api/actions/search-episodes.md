# Search Episodes with STAPI

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/rest/episode/search`
- **Base URL:** `https://stapi.co/api`
- **Official documentation:** [Search Episodes](https://stapi.co/api-documentation)

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
| `title` | body | `string` | no | Episode title |
