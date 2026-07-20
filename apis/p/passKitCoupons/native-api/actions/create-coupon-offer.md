# Create Coupon Offer with PassKit Coupons

## Endpoint

- **Method:** `POST`
- **Path:** `/coupon/singleUse/offer`
- **Base URL:** `https://api.pub2.passkit.io`
- **Official documentation:** [Create Coupon Offer](https://docs.passkit.io/protocols/coupon/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `beforeRedeemPassTemplateId` | body | `string` | no | Pass template ID used before redemption. |
| `campaignId` | body | `string` | no | Coupon campaign ID for this offer when applicable. |
| `issueEndDate` | body | `string` | no | Offer issuance end date in RFC3339 format. |
| `issueStartDate` | body | `string` | no | Offer issuance start date in RFC3339 format. |
| `offerDetails` | body | `string` | no | Offer details shown on the coupon offer. |
| `offerShortTitle` | body | `string` | no | Short title for the coupon offer. |
| `offerTitle` | body | `string` | no | Offer title for the coupon offer. |
