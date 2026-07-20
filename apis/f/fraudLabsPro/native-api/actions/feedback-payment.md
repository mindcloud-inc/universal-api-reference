# Feedback Payment with FraudLabs Pro

Updates payment feedback in FraudLabs Pro.

## Endpoint

- **Method:** `POST`
- **Path:** `v2/payment/feedback`
- **Base URL:** `https://api.fraudlabspro.com/`
- **Official documentation:** [Feedback Payment](https://www.fraudlabspro.com/developer/api/feedback-payment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The email address tied to the payment order. |
| `status` | body | `string` | yes | The final payment status. |
| `message` | body | `string` | yes | The message returned from the payment gateway. |
| `fraudlabspro_id` | body | `string` | no | The FraudLabs Pro transaction ID. |
