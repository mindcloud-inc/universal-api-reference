# List Models with Hightouch

Retrieves models from Hightouch.

## Endpoint

- **Method:** `GET`
- **Path:** `/models`
- **Base URL:** `https://api.hightouch.com/api/v1`
- **Official documentation:** [List Models](https://api.hightouch.io/api/swagger.json)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Filter models by name. |
| `slug` | query | `string` | no | Filter models by slug. |
| `tags` | query | `string` | no | Filter models by tags. |
