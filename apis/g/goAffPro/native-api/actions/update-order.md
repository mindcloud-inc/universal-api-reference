# Update Order with GoAffPro

Updates an existing order in GoAffPro.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/admin/orders/:id`
- **Base URL:** `https://api.goaffpro.com/v1`
- **Official documentation:** [Update Order](https://api.goaffpro.com/docs/admin/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Order ID. |
| `status` | body | `string` | no | Order status. |
| `commission` | body | `number` | no | Commission amount. |
