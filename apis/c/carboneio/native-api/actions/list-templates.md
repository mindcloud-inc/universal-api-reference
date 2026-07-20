# List Templates with Carbone.io

Retrieves templates from Carbone.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/templates`
- **Base URL:** `https://api.carbone.io`
- **Official documentation:** [List Templates](https://carbone.io/documentation/developer/http-api/manage-templates.html#list-templates)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | query | `string` | no | Filter results to templates in one category. |
| `id` | query | `string` | no | Filter results to one Carbone template ID. |
| `includeVersions` | query | `boolean` | no | Include all versions for a specific template ID. |
| `origin` | query | `number` | no | Filter by template upload origin: 0 for API uploads or 1 for Studio uploads. |
| `search` | query | `string` | no | Search template names, template IDs, or version IDs. |
| `versionId` | query | `string` | no | Filter results to one template version ID. |
