# Send LinkedIn Message with GetSales.io

## Endpoint

- **Method:** `POST`
- **Path:** `/flows/api/linkedin-messages`
- **Base URL:** `https://amazing.getsales.io`
- **Official documentation:** [Send LinkedIn Message](https://api.getsales.io/api/openapi/unibox/sendlinkedinmessage.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sender_profile_uuid` | body | `string` | no | Sender profile UUID. |
| `lead_uuid` | body | `string` | no | Contact UUID. |
| `template_uuid` | body | `string` | no | Template UUID for the message. |
| `text` | body | `string` | no | LinkedIn message text. |
| `attachments[]` | body | `array<object>` | no | Attachment array. |
