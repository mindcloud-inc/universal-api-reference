# Send SMS with ExpertTexting

Creates an SMS message in ExpertTexting.

## Endpoint

- **Method:** `POST`
- **Path:** `/ExptRestApi/sms/json/Message/Send`
- **Base URL:** `https://www.experttexting.com`
- **Official documentation:** [Send SMS](https://www.experttexting.com/appv2/Documentation/Send)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | yes | Sender ID or DEFAULT for reliable delivery. |
| `to` | body | `string` | yes | Recipient number in international E.164 format without + or 00. |
| `text` | body | `string` | yes | SMS body text, UTF-8 and URL-encoded by the platform. |
