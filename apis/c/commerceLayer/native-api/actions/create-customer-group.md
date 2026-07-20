# Create Customer Group with Commerce Layer

## Endpoint

- **Method:** `POST`
- **Path:** `/api/customer_groups`
- **Base URL:** `{coreApiEndpoint}`
- **Official documentation:** [Create Customer Group](https://docs.commercelayer.io/core-api-reference/customer_groups/create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data.attributes.name` | body | `string` | yes |
| `data.attributes.code` | body | `string` | no |
| `data.attributes.reference` | body | `string` | no |
| `data.attributes.reference_origin` | body | `string` | no |
