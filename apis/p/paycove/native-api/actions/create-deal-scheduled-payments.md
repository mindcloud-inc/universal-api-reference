# Create Deal Scheduled Payments with Paycove

Creates scheduled payments for a Paycove deal.

## Endpoint

- **Method:** `POST`
- **Path:** `add-scheduled-payments/:deal_id`
- **Base URL:** `https://paycove.io/api/v1`
- **Official documentation:** [Create Deal Scheduled Payments](https://docs.paycove.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deal_id` | path | `string` | yes | Paycove deal id. |
| `scheduledPayments[]` | body | `array<object>` | yes | Array of scheduled payment objects to create for the deal. |
