# Update an existing category or category group with Lunch Money

## Endpoint

- **Method:** `PUT`
- **Path:** `/categories/:id`
- **Base URL:** `https://api.lunchmoney.dev/v2`
- **Official documentation:** [Update an existing category or category group](https://alpha.lunchmoney.dev/v2/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `name` | body | `string` | no |
| `description` | body | `string` | no |
| `archived` | body | `boolean` | no |
