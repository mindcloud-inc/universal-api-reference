# List Folder Templates with Templated

Retrieves templates in a folder from Templated.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/folder/:id/templates`
- **Base URL:** `https://api.templated.io`
- **Official documentation:** [List Folder Templates](https://templated.io/docs/folders/templates/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The folder id that you want to retrieve the templates. |
| `query` | query | `string` | no | Filter templates by name. |
| `width` | query | `number` | no | Filter templates by width. |
| `height` | query | `number` | no | Filter templates by height. |
| `tags` | query | `string` | no | Filter templates by tags. |
| `includeLayers` | query | `boolean` | no | Include template layers in the response. |
