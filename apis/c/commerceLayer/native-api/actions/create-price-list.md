# Create Price List with Commerce Layer

## Endpoint

- **Method:** `POST`
- **Path:** `/api/price_lists`
- **Base URL:** `{coreApiEndpoint}`
- **Official documentation:** [Create Price List](https://docs.commercelayer.io/core-api-reference/price_lists/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.attributes.name` | body | `string` | yes | The price list name. |
| `data.attributes.code` | body | `string` | no | An optional code for the price list. |
| `data.attributes.currency_code` | body | `string` | yes | The ISO currency code for the price list. |
| `data.attributes.tax_included` | body | `boolean` | no | Whether prices include tax. |
| `data.attributes.reference` | body | `string` | no | An external reference for the price list. |
| `data.attributes.reference_origin` | body | `string` | no | The origin of the external reference. |
