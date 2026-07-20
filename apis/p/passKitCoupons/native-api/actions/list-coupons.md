# List Coupons with PassKit Coupons

## Endpoint

- **Method:** `POST`
- **Path:** `/coupon/singleUse/coupons/list/:couponCampaignId`
- **Base URL:** `https://api.pub2.passkit.io`
- **Official documentation:** [List Coupons](https://docs.passkit.io/protocols/coupon/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `couponCampaignId` | path | `string` | yes | Coupon campaign ID. |
| `emailAsCsv` | body | `boolean` | no | Email the coupon list as a CSV instead of returning it directly. |
| `filters.limit` | body | `number` | no | Maximum number of coupons to return. |
| `filters.offset` | body | `number` | no | Number of coupon records to skip. |
