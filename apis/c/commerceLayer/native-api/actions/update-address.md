# Update Address with Commerce Layer

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/addresses/:id`
- **Base URL:** `{coreApiEndpoint}`
- **Official documentation:** [Update Address](https://docs.commercelayer.io/core-api-reference/addresses/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The address ID to update. |
| `data.id` | body | `string` | yes | The address resource ID in the JSON:API body. Use the same value as Address ID. |
| `data.attributes.first_name` | body | `string` | no | The updated first name. |
| `data.attributes.last_name` | body | `string` | no | The updated last name. |
| `data.attributes.phone` | body | `string` | no | The updated phone number. |
| `data.attributes.email` | body | `string` | no | The updated email address. |
| `data.attributes.notes` | body | `string` | no | The updated notes. |
