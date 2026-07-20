# Update Customer Group with Commerce Layer

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/customer_groups/:id`
- **Base URL:** `{coreApiEndpoint}`
- **Official documentation:** [Update Customer Group](https://docs.commercelayer.io/core-api-reference/customer_groups/update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `data.id` | body | `string` | yes |
| `data.attributes.name` | body | `string` | no |
| `data.attributes.code` | body | `string` | no |
| `data.attributes.reference` | body | `string` | no |
| `data.attributes.reference_origin` | body | `string` | no |
