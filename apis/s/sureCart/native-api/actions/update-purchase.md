# Update Purchase with SureCart

## Endpoint

- **Method:** `PATCH`
- **Path:** `v1/purchases/:id`
- **Base URL:** `https://api.surecart.com`
- **Official documentation:** [Update Purchase](https://developer.surecart.com/api-reference/purchases/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The purchase ID to update. |
| `purchase.revoke_at` | body | `string` | yes | When the purchase should be revoked, for example 2026-04-05 00:00:00 UTC. |
