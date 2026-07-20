# Send HTML Email with Lettr

## Endpoint

- **Method:** `POST`
- **Path:** `/emails`
- **Base URL:** `https://app.lettr.com/api/`
- **Official documentation:** [Send HTML Email](https://docs.lettr.com/api-reference/emails/send-email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | no | Sender email address. |
| `html` | body | `string` | no | HTML email body. |
| `subject` | body | `string` | no | Email subject line. |
| `to` | body | `string` | no | Recipient email addresses. |
