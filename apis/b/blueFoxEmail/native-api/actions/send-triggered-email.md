# Send Triggered Email with BlueFox Email

Sends a triggered email through BlueFox Email.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/send-triggered`
- **Base URL:** `https://api.bluefox.email`
- **Official documentation:** [Send Triggered Email](https://bluefox.email/docs/api/send-triggered-email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails[]` | body | `array<string>` | no | Optional recipient email addresses for the triggered email. If omitted, BlueFox sends to all subscribers in the linked list. |
| `triggeredId` | body | `string` | yes | BlueFox triggered email ID. |
