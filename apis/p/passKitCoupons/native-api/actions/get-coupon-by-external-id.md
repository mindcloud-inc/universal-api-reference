# Get Coupon by External ID with PassKit Coupons

## Endpoint

- **Method:** `GET`
- **Path:** `/coupon/singleUse/coupon/externalId/:couponCampaignId/:externalId`
- **Base URL:** `https://api.pub2.passkit.io`
- **Official documentation:** [Get Coupon by External ID](https://docs.passkit.io/protocols/coupon/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `couponCampaignId` | path | `string` | yes | Coupon campaign ID. |
| `externalId` | path | `string` | yes | External ID for the coupon. |
