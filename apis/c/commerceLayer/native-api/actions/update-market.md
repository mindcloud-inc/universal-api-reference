# Update Market with Commerce Layer

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/markets/:id`
- **Base URL:** `{coreApiEndpoint}`
- **Official documentation:** [Update Market](https://docs.commercelayer.io/core-api-reference/markets/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The market ID to update. |
| `data.id` | body | `string` | yes | The market resource ID in the JSON:API body. Use the same value as Market ID. |
| `data.attributes.name` | body | `string` | no | The updated market name. |
| `data.attributes.code` | body | `string` | no | The updated market code. |
| `data.attributes.reference` | body | `string` | no | The updated external reference. |
| `data.attributes.reference_origin` | body | `string` | no | The updated reference origin. |
