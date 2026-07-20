# Send Draft Email with Buttondown

Sends a draft email from Buttondown to specific recipients.

## Endpoint

- **Method:** `POST`
- **Path:** `/emails/:id/send-draft`
- **Base URL:** `https://api.buttondown.com/v1`
- **Official documentation:** [Send Draft Email](https://docs.buttondown.com/api-emails-send-draft)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Email ID. |
| `recipients[]` | body | `array<string>` | yes | Explicit recipient email addresses for the draft send. |
