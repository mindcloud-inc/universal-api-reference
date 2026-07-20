# List Models with HeadshotPro

Retrieves models from HeadshotPro.

## Endpoint

- **Method:** `GET`
- **Path:** `/organization/models`
- **Base URL:** `https://server.headshotpro.com/api/v2`
- **Official documentation:** [List Models](https://www.headshotpro.com/api/models)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Optional model status filter. |
| `teamId` | query | `string` | no | Optional team filter. |
