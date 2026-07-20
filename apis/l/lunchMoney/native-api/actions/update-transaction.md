# Update an existing transaction with Lunch Money

## Endpoint

- **Method:** `PUT`
- **Path:** `/transactions/:id`
- **Base URL:** `https://api.lunchmoney.dev/v2`
- **Official documentation:** [Update an existing transaction](https://alpha.lunchmoney.dev/v2/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `notes` | body | `string` | no |
| `payee` | body | `string` | no |
