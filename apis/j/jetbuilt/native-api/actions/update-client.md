# Update Client with Jetbuilt

## Endpoint

- **Method:** `PATCH`
- **Path:** `clients/:id`
- **Base URL:** `https://app.jetbuilt.com/api/`
- **Official documentation:** [Update Client](https://api.jetbuilt.com/customers#update-a-client)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `external_ids` | body | `object` | no | Use this object to associate any other Id |
| `id` | path | `number` | no | — |
| `city` | body | `string` | no | — |
| `country` | body | `string` | no | — |
| `description` | body | `string` | no | — |
| `parent_id` | body | `string` | no | — |
| `phone` | body | `string` | no | — |
| `state` | body | `string` | no | — |
| `street_address` | body | `string` | no | — |
| `user_id` | body | `string` | no | — |
| `website` | body | `string` | no | — |
| `zipcode` | body | `string` | no | — |
| `company_name` | body | `string` | no | — |
| `owner.id` | body | `string` | no | — |
| `owner.name` | body | `string` | no | — |
| `metadata` | body | `object` | no | — |
| `owner` | body | `object` | no | — |
