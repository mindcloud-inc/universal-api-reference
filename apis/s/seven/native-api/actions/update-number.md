# Update Number with Seven

Updates an active number in Seven.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/numbers/active/:number`
- **Base URL:** `https://gateway.seven.io/api`
- **Official documentation:** [Update Number](https://docs.seven.io/en/rest-api/endpoints/numbers#update-number)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | path | `string` | yes | The phone number to update details for. |
| `friendly_name` | body | `string` | no | The updated friendly name for the number. |
| `sms_forward[]` | body | `array<string>` | no | The phone number to forward incoming SMS to. If empty, incoming SMS won&#x27;t be forwarded by SMS. |
| `email_forward[]` | body | `array<string>` | no | The email address to forward incoming SMS to. If empty, incoming SMS won&#x27;t be forwarded by email. |
| `slack_forward` | body | `string` | no | The Slack webhook URL to forward incoming SMS to. If empty, incoming SMS won&#x27;t be forwarded by Slack. |
