# Refund Sale with Gumroad

Refunds a sale in Gumroad.

## Endpoint

- **Method:** `PUT`
- **Path:** `/sales/:id/refund`
- **Base URL:** `https://api.gumroad.com/v2`
- **Official documentation:** [Refund Sale](https://gumroad.com/api#put-/sales/:id/refund)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The sale ID. |
| `amount_cents` | body | `number` | no | Issue a partial refund for this amount in cents. |
