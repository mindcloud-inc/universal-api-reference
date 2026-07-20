# List Mdoc Credential Templates with Paradym

Retrieves mdoc credential templates from Paradym.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/templates/credentials/mdoc`
- **Base URL:** `https://api.paradym.id/v1`
- **Official documentation:** [List Mdoc Credential Templates](https://paradym.id/reference#tag/mdoc-credential-templates)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search[name]` | query | `string` | no | Search templates by name. |
| `filter[type]` | query | `string` | no | Filter templates by credential type. |
| `filter[archived]` | query | `boolean` | no | Filter templates by archived state. |
