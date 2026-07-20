# Send Email with GetSales.io

## Endpoint

- **Method:** `POST`
- **Path:** `/emails/api/emails/send-email`
- **Base URL:** `https://amazing.getsales.io`
- **Official documentation:** [Send Email](https://api.getsales.io/api/openapi/unibox/sendemail.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sender_profile_uuid` | body | `string` | no | Sender profile UUID. |
| `lead_uuid` | body | `string` | no | Contact UUID. |
| `from_name` | body | `string` | no | Sender display name. |
| `from_email` | body | `string` | no | Sender email address. |
| `to_name` | body | `string` | no | Recipient display name. |
| `to_email` | body | `string` | no | Recipient email address. |
| `subject` | body | `string` | no | Email subject. |
