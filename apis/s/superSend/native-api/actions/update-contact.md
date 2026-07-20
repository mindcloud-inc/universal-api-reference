# Update Contact with SuperSend

Updates an existing contact in SuperSend.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contacts/{id}`
- **Base URL:** `https://api.supersend.io/v2`
- **Official documentation:** [Update Contact](https://docs.supersend.io/docs/contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Resource ID (UUID) |
| `first_name` | body | `string` | no | — |
| `last_name` | body | `string` | no | — |
| `company` | body | `string` | no | — |
| `title` | body | `string` | no | — |
| `phone` | body | `string` | no | — |
| `website` | body | `string` | no | — |
| `interest` | body | `string` | no | — |
| `custom` | body | `object` | no | — |
