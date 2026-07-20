# List Template Renders with Templated

Retrieves renders for a template in Templated.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/template/:id/renders`
- **Base URL:** `https://api.templated.io`
- **Official documentation:** [List Template Renders](https://templated.io/docs/templates/renders/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The template id that you want to retrieve the renders. |
| `externalId` | query | `string` | no | Filter renders by external ID. |
