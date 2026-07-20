# Update Coupon with Soundee

Updates an existing coupon in Soundee.

## Endpoint

- **Method:** `PUT`
- **Path:** `/coupons/:id`
- **Base URL:** `https://api.soundee.com/me`
- **Official documentation:** [Update Coupon](https://soundee.readme.io/reference/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The ID of the coupon to update. |
| `name` | body | `string` | no | The name or code of the coupon. |
| `amount` | body | `number` | no | The discount amount. |
| `upgrades` | body | `string` | no | Whether the coupon applies to upgrades. |
| `active` | body | `boolean` | no | Enable or disable the coupon. |
| `maxUsage` | body | `number` | no | Maximum total uses for the coupon. |
| `type` | body | `string` | no | The discount type. |
| `minCartItems` | body | `number` | no | Minimum number of cart items required. |
| `minCartAmount` | body | `number` | no | Minimum cart total required. |
| `stopBulkDiscounts` | body | `boolean` | no | Stop further bulk discounts when this coupon applies. |
| `startDate` | body | `string` | no | When the coupon becomes active. |
| `endDate` | body | `string` | no | When the coupon expires. |
| `neverEnd` | body | `boolean` | no | Ignore the end date. |
| `conditions` | body | `object` | no | Conditions that define which stores, licenses, entity types, or entities the coupon applies to. |
