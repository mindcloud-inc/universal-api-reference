# List Presentation Templates with Paradym

Retrieves presentation templates from Paradym.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/templates/presentations`
- **Base URL:** `https://api.paradym.id/v1`
- **Official documentation:** [List Presentation Templates](https://paradym.id/reference#tag/presentation-templates)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search[name]` | query | `string` | no | Search presentation templates by name. |
