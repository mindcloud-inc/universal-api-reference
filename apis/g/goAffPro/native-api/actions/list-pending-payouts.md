# List Pending Payouts with GoAffPro

Retrieves pending affiliate payouts from GoAffPro.

## Endpoint

- **Method:** `GET`
- **Path:** `/admin/payments/pending`
- **Base URL:** `https://api.goaffpro.com/v1`
- **Official documentation:** [List Pending Payouts](https://api.goaffpro.com/docs/admin/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `affiliate_id` | query | `string` | no | Only return pending payout amounts for this affiliate ID. |
