# List Upcoming Payouts with Gumroad

Retrieves upcoming payouts from Gumroad.

## Endpoint

- **Method:** `GET`
- **Path:** `/payouts/upcoming`
- **Base URL:** `https://api.gumroad.com/v2`
- **Official documentation:** [List Upcoming Payouts](https://gumroad.com/api#get-/payouts/upcoming)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_sales` | query | `boolean` | no | Set to false to exclude sales details from the response. |
| `include_transactions` | query | `boolean` | no | Set to true to include payout transaction details. |
