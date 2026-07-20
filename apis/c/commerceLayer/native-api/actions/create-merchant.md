# Create Merchant with Commerce Layer

## Endpoint

- **Method:** `POST`
- **Path:** `/api/merchants`
- **Base URL:** `{coreApiEndpoint}`
- **Official documentation:** [Create Merchant](https://docs.commercelayer.io/core-api-reference/merchants/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.attributes.name` | body | `string` | yes | The merchant name. |
| `data.attributes.reference` | body | `string` | no | An external reference for the merchant. |
| `data.attributes.reference_origin` | body | `string` | no | The origin of the external reference. |
| `data.relationships.address.data.id` | body | `string` | yes | The ID of the address to link to this merchant. |
