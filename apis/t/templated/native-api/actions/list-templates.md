# List Templates with Templated

Retrieves all template records from Templated.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/templates`
- **Base URL:** `https://api.templated.io`
- **Official documentation:** [List Templates](https://templated.io/docs/templates/list/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | no | Filter templates by name. |
| `width` | query | `number` | no | Filter templates by width. |
| `height` | query | `number` | no | Filter templates by height. |
| `tags` | query | `string` | no | Filter templates by comma-separated tags. |
| `externalId` | query | `string` | no | Filter templates by external ID. |
| `includeLayers` | query | `boolean` | no | Include template layers in the response. |
| `includePages` | query | `boolean` | no | Include template pages and layers in the response. |
