# Get Active Campaigns with Yotpo Loyalty & Referrals

Retrieves active campaigns from Yotpo Loyalty & Referrals.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/campaigns`
- **Base URL:** `https://loyalty.yotpo.com`
- **Official documentation:** [Get Active Campaigns](https://loyaltyapi.yotpo.com/reference/get-active-campaigns)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `with_status` | query | `boolean` | no | Include status information when set to true. |
| `customer_email` | query | `string` | no | Filter campaigns for a specific customer email. |
| `customer_id` | query | `string` | no | Filter campaigns for a specific customer ID. |
