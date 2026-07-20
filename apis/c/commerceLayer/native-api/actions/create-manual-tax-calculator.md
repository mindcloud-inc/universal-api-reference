# Create Manual Tax Calculator with Commerce Layer

## Endpoint

- **Method:** `POST`
- **Path:** `/api/manual_tax_calculators`
- **Base URL:** `{coreApiEndpoint}`
- **Official documentation:** [Create Manual Tax Calculator](https://docs.commercelayer.io/core-api-reference/manual_tax_calculators/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.attributes.name` | body | `string` | yes | The manual tax calculator name. |
| `data.attributes.reference` | body | `string` | no | An external reference for the manual tax calculator. |
| `data.attributes.reference_origin` | body | `string` | no | The origin of the external reference. |
