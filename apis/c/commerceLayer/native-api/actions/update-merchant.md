# Update Merchant with Commerce Layer

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/merchants/:id`
- **Base URL:** `{coreApiEndpoint}`
- **Official documentation:** [Update Merchant](https://docs.commercelayer.io/core-api-reference/merchants/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The merchant ID to update. |
| `data.id` | body | `string` | yes | Use the same merchant ID in the request body resource object. |
| `data.attributes.name` | body | `string` | no | The updated merchant name. |
| `data.attributes.reference` | body | `string` | no | The updated external reference. |
| `data.attributes.reference_origin` | body | `string` | no | The updated external reference origin. |
