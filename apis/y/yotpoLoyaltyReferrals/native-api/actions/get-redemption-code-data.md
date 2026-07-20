# Get Redemption Code Data with Yotpo Loyalty & Referrals

Retrieves redemption code data from Yotpo Loyalty & Referrals.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/redemption_codes`
- **Base URL:** `https://loyalty.yotpo.com`
- **Official documentation:** [Get Redemption Code Data](https://loyaltyapi.yotpo.com/reference/get-redemption-code-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `third_party_id` | query | `string` | no | Third-party unique identifier for the redemption code. |
| `code` | query | `string` | no | Discount code to look up. |
