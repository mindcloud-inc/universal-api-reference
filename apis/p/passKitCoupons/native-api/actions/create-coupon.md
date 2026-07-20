# Create Coupon with PassKit Coupons

## Endpoint

- **Method:** `POST`
- **Path:** `/coupon/singleUse/coupon`
- **Base URL:** `https://api.pub2.passkit.io`
- **Official documentation:** [Create Coupon](https://docs.passkit.io/protocols/coupon/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | body | `string` | no | Coupon campaign ID to issue under. |
| `externalId` | body | `string` | no | External identifier for the coupon holder or coupon record. |
| `offerId` | body | `string` | no | Coupon offer ID to issue from. |
| `sku` | body | `string` | no | SKU value for the issued coupon. |
