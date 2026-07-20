# Redeem an Item with Absinthe

Redeems a reward item for a user in Absinthe.

## Endpoint

- **Method:** `POST`
- **Path:** `/redemptions/users/{user_id}/redeem`
- **Base URL:** `https://api.absinthe.network`
- **Official documentation:** [Redeem an Item](https://api.absinthe.network/doc)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `user_id` | path | `string` | yes |
| `inventory_item_id` | body | `string` | yes |
