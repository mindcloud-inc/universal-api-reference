# Count Coupons with PassKit Coupons

## Endpoint

- **Method:** `POST`
- **Path:** `/coupon/singleUse/coupons/count/:couponCampaignId`
- **Base URL:** `https://api.pub2.passkit.io`
- **Official documentation:** [Count Coupons](https://docs.passkit.io/protocols/coupon/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `couponCampaignId` | path | `string` | yes | Coupon campaign ID. |
| `emailAsCsv` | body | `boolean` | no | Return matching coupon emails as CSV when true. |
