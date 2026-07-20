# Create Shipping Category with Commerce Layer

## Endpoint

- **Method:** `POST`
- **Path:** `/api/shipping_categories`
- **Base URL:** `{coreApiEndpoint}`
- **Official documentation:** [Create Shipping Category](https://docs.commercelayer.io/core-api-reference/shipping_categories/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.attributes.name` | body | `string` | yes | The shipping category name. |
| `data.attributes.code` | body | `string` | no | An optional code for the shipping category. |
| `data.attributes.reference` | body | `string` | no | An external reference for the shipping category. |
| `data.attributes.reference_origin` | body | `string` | no | The origin of the external reference. |
