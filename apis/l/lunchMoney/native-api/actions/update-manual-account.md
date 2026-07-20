# Update an existing manual account with Lunch Money

## Endpoint

- **Method:** `PUT`
- **Path:** `/manual_accounts/:id`
- **Base URL:** `https://api.lunchmoney.dev/v2`
- **Official documentation:** [Update an existing manual account](https://alpha.lunchmoney.dev/v2/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `display_name` | body | `string` | no |
| `balance` | body | `number` | no |
