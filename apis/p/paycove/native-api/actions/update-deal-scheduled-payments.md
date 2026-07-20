# Update Deal Scheduled Payments with Paycove

Updates scheduled payments for a Paycove deal.

## Endpoint

- **Method:** `PATCH`
- **Path:** `update-scheduled-payments/:deal_id`
- **Base URL:** `https://paycove.io/api/v1`
- **Official documentation:** [Update Deal Scheduled Payments](https://docs.paycove.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deal_id` | path | `string` | yes | Paycove deal id. |
| `scheduledPayments[]` | body | `array<object>` | yes | Array of scheduled payment objects to replace for the deal. |
