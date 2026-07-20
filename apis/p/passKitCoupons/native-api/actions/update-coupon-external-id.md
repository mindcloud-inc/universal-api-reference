# Update Coupon External Id with PassKit Coupons

## Endpoint

- **Method:** `PUT`
- **Path:** `/coupon/singleUse/coupon/externalId`
- **Base URL:** `https://api.pub2.passkit.io`
- **Official documentation:** [Update Coupon External Id](https://docs.passkit.io/protocols/coupon/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `couponCampaignId` | body | `string` | no | Coupon campaign ID when identifying by external ID. |
| `externalId` | body | `string` | no | Existing external ID to replace. |
| `id` | body | `string` | no | PassKit coupon ID to update. |
| `newExternalId` | body | `string` | no | Replacement external ID for the coupon. |
