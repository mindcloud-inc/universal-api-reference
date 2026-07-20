# Create Coupon with Checkout Page

Creates a coupon in Checkout Page.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/coupons/`
- **Base URL:** `https://api.checkoutpage.com`
- **Official documentation:** [Create Coupon](https://checkoutpage.com/docs/api/v1/coupons/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `label` | body | `string` | yes | Internal name for the coupon. |
| `code` | body | `string` | yes | The coupon code a customer enters. |
| `amountOff` | body | `number` | no | A positive integer representing the amount to subtract from an invoice total (required if `percentOff` is not passed). |
| `currency` | body | `string` | no | Three-letter ISO code for the currency of the amountOff parameter (required if `amountOff` is passed). |
| `duration` | body | `string` | yes | — |
| `durationInMonths` | body | `number` | no | A positive integer representing the number of months the coupon applies for (required if `duration === repeating`) |
| `percentOff` | body | `number` | no | A positive float larger than 0, and smaller or equal to 100, that represents the discount the coupon will apply (required if `amountOff` is not passed). |
| `appliesToSetupFee` | body | `boolean` | no | When enabled, applies this coupon discount to the setup fee. |
| `pageIds[]` | body | `array<string>` | no | A list of pageIds that this coupon can be used within. |
| `ticketTypeIds[]` | body | `array<string>` | no | List of ticket type IDs that this coupon can be used with. Ticket ticket ids must belong to a page specified in the `pageIds` array. |
| `maxRedemptions` | body | `number` | no | The total amount of times this coupon can be used. Doesn't limit a single customer from redeeming multiple times. |
| `redeemBy` | body | `date` | no | The ISO datetime that this coupon must be used before. |
