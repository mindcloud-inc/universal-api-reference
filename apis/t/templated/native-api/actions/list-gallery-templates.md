# List Gallery Templates with Templated

Retrieves gallery template records from Templated.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/templates/gallery`
- **Base URL:** `https://api.templated.io`
- **Official documentation:** [List Gallery Templates](https://templated.io/docs/templates/gallery/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Search gallery templates by name or description. |
| `category` | query | `string` | no | Filter gallery templates by category name. |
| `tags` | query | `string` | no | Filter gallery templates by comma-separated tags. |
| `width` | query | `number` | no | Filter gallery templates by exact width. |
| `height` | query | `number` | no | Filter gallery templates by exact height. |
| `includeLayers` | query | `boolean` | no | Include gallery template layers in the response. |
