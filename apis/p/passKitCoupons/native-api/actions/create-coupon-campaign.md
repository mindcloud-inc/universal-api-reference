# Create Coupon Campaign with PassKit Coupons

## Endpoint

- **Method:** `POST`
- **Path:** `/coupon/singleUse/campaign`
- **Base URL:** `https://api.pub2.passkit.io`
- **Official documentation:** [Create Coupon Campaign](https://docs.passkit.io/protocols/coupon/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endDate` | body | `string` | no | Campaign end date. |
| `name` | body | `string` | no | Name of the coupon campaign. |
| `offerId` | body | `string` | no | Offer ID associated with the campaign. |
| `startDate` | body | `string` | no | Campaign start date. |
| `status` | body | `string` | no | Project status flags for the campaign. |
