# List Ideas with ProdPad

Retrieves ideas from ProdPad.

## Endpoint

- **Method:** `GET`
- **Path:** `/ideas`
- **Base URL:** `https://api.prodpad.com/v1`
- **Official documentation:** [List Ideas](https://app.swaggerhub.com/apis-docs/ProdPad/prodpad/1.1.4#/Ideas/GetIdeas)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tags` | query | `string` | no | Send multiple values as a string separated by `,`. |
| `product` | query | `string` | no | — |
| `persona` | query | `string` | no | — |
| `status` | query | `string` | no | — |
| `state` | query | `string` | no | — |
| `external_id` | query | `string` | no | — |
| `external_url` | query | `string` | no | — |
| `withfeedback` | query | `boolean` | no | Return associated feedback with each idea. |
