# Create Refund with SureCart

## Endpoint

- **Method:** `POST`
- **Path:** `v1/refunds`
- **Base URL:** `https://api.surecart.com`
- **Official documentation:** [Create Refund](https://developer.surecart.com/api-reference/refunds/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `refund.amount` | body | `number` | yes | Refund amount in cents. |
| `refund.reason` | body | `string` | yes | Refund reason, for example requested_by_customer. |
| `refund.charge_id` | body | `string` | yes | The charge ID to refund. |
