# Create SKU with Commerce Layer

## Endpoint

- **Method:** `POST`
- **Path:** `/api/skus`
- **Base URL:** `{coreApiEndpoint}`
- **Official documentation:** [Create SKU](https://docs.commercelayer.io/core-api-reference/skus/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.attributes.code` | body | `string` | yes | The SKU code. |
| `data.attributes.name` | body | `string` | yes | The SKU name. |
| `data.attributes.reference` | body | `string` | no | An external reference for the SKU. |
