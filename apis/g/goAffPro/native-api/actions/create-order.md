# Create Order with GoAffPro

Creates a manual affiliate order and commission in GoAffPro.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/orders`
- **Base URL:** `https://api.goaffpro.com/v1`
- **Official documentation:** [Create Order](https://api.goaffpro.com/docs/admin/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order.number` | body | `string` | yes | Order number to display. |
| `order.total` | body | `number` | yes | Total order value. |
| `affiliate_id` | body | `string` | no | Affiliate ID to assign the order to. |
| `ref_code` | body | `string` | no | Referral code used in the order. |
