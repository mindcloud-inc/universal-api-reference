# Upload Coupon Codes with Yotpo Loyalty & Referrals

Uploads coupon codes to Yotpo Loyalty & Referrals.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/redemption_codes`
- **Base URL:** `https://loyalty.yotpo.com`
- **Official documentation:** [Upload Coupon Codes](https://loyaltyapi.yotpo.com/reference/add-coupon-codes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `redemption_option_id` | body | `number` | yes | Redemption option ID returned by the active redemption options endpoint. |
| `codes` | body | `string` | yes | Comma-separated coupon codes to upload. Up to 10,000 codes are allowed. |
