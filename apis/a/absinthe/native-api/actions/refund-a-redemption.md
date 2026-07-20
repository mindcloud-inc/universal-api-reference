# Refund a Redemption with Absinthe

Refunds a redemption for a user in Absinthe.

## Endpoint

- **Method:** `POST`
- **Path:** `/redemptions/{redemption_id}/refund`
- **Base URL:** `https://api.absinthe.network`
- **Official documentation:** [Refund a Redemption](https://api.absinthe.network/doc)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `redemption_id` | path | `string` | no |
| `refund_reason` | body | `string` | yes |
