# Get Active Redemption Options with Yotpo Loyalty & Referrals

Retrieves active redemption options from Yotpo Loyalty & Referrals.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/redemption_options`
- **Base URL:** `https://loyalty.yotpo.com`
- **Official documentation:** [Get Active Redemption Options](https://loyaltyapi.yotpo.com/reference/fetch-active-redemption-options)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `is_offline` | query | `string` | no | Filter redemption options by offline availability. |
| `customer_email` | query | `string` | no | Filter redemption options for a specific customer email. |
| `customer_id` | query | `string` | no | Filter redemption options for a specific customer ID. |
| `phone_number` | query | `string` | no | Filter redemption options for a specific phone number. |
| `discount_type` | query | `string` | no | Filter redemption options by discount type. |
