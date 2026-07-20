# List Coupon Offers with PassKit Coupons

## Endpoint

- **Method:** `POST`
- **Path:** `/coupon/singleUse/offers/list`
- **Base URL:** `https://api.pub2.passkit.io`
- **Official documentation:** [List Coupon Offers](https://docs.passkit.io/protocols/coupon/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | body | `string` | no | Campaign ID to scope the offer list. |
| `filters.limit` | body | `number` | no | Maximum number of offers to return. |
| `filters.offset` | body | `number` | no | Number of offer records to skip. |
