# Adjust Customer Points Balance with Yotpo Loyalty & Referrals

Updates a customer's points balance in Yotpo Loyalty & Referrals.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/points/adjust`
- **Base URL:** `https://loyalty.yotpo.com`
- **Official documentation:** [Adjust Customer Points Balance](https://loyaltyapi.yotpo.com/reference/adjust-a-customers-point-balance)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_email` | body | `string` | no | Customer email address. Required if customerId is not provided. |
| `customer_id` | body | `string` | no | Customer identifier from your system. |
| `point_adjustment_amount` | body | `number` | yes | Positive values add points and negative values remove points. |
| `apply_adjustment_to_points_earned` | body | `boolean` | no | Whether the adjustment should also change the customer's total points earned value. |
| `history_title` | body | `string` | no | Optional override for the history description shown to the customer. |
| `visible_to_customer` | body | `boolean` | no | Whether the manual adjustment should be visible to the customer. |
