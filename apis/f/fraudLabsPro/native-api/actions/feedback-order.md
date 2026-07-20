# Feedback Order with FraudLabs Pro

Updates order feedback in FraudLabs Pro.

## Endpoint

- **Method:** `POST`
- **Path:** `v2/order/feedback`
- **Base URL:** `https://api.fraudlabspro.com/`
- **Official documentation:** [Feedback Order](https://www.fraudlabspro.com/developer/api/feedback-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The FraudLabs Pro transaction ID or merchant order ID. |
| `action` | body | `string` | yes | Feedback action to send. Accepted values: `0`, `1`, `2`. |
