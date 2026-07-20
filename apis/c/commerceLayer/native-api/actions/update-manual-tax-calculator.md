# Update Manual Tax Calculator with Commerce Layer

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/manual_tax_calculators/:id`
- **Base URL:** `{coreApiEndpoint}`
- **Official documentation:** [Update Manual Tax Calculator](https://docs.commercelayer.io/core-api-reference/manual_tax_calculators/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The manual tax calculator ID to update. |
| `data.id` | body | `string` | yes | Use the same manual tax calculator ID in the request body resource object. |
| `data.attributes.name` | body | `string` | no | The updated manual tax calculator name. |
| `data.attributes.reference` | body | `string` | no | The updated external reference. |
| `data.attributes.reference_origin` | body | `string` | no | The updated external reference origin. |
