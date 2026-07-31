# Search Characters with STAPI

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/rest/character/search`
- **Base URL:** `https://stapi.co/api`
- **Official documentation:** [Search Characters](https://stapi.co/api-documentation)

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
| `name` | body | `string` | no | Character name |
