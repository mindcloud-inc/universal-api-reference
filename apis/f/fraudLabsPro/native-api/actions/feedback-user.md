# Feedback User with FraudLabs Pro

Updates user feedback in FraudLabs Pro.

## Endpoint

- **Method:** `POST`
- **Path:** `v2/user/feedback`
- **Base URL:** `https://api.fraudlabspro.com/`
- **Official documentation:** [Feedback User](https://www.fraudlabspro.com/developer/api/feedback-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The FraudLabs Pro user transaction ID or merchant user ID. |
| `action` | body | `string` | yes | Feedback action to send. Accepted values: `0`, `1`, `2`. |
