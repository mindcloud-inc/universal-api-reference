# Approve Redemption Cancellation with Yotpo Loyalty & Referrals

Approves a redemption cancellation in Yotpo Loyalty & Referrals.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/redemptions/:point_redemption_id/cancellation_completed`
- **Base URL:** `https://loyalty.yotpo.com`
- **Official documentation:** [Approve Redemption Cancellation](https://loyaltyapi.yotpo.com/reference/approve-redemption-cancellation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `point_redemption_id` | path | `number` | yes | The redemption identifier to approve. |
| `reward_text` | body | `string` | yes | The reward text of the redemption being cancelled. |
