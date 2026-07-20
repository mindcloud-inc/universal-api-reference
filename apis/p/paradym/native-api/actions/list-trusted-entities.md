# List Trusted Entities with Paradym

Retrieves a list of trusted entities from Paradym.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/trusted-entities`
- **Base URL:** `https://api.paradym.id/v1`
- **Official documentation:** [List Trusted Entities](https://paradym.id/reference#tag/trusted-entities)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search[name]` | query | `string` | no | Search trusted entities by name. |
