# Schedule Email with Lettr

## Endpoint

- **Method:** `POST`
- **Path:** `/emails/scheduled`
- **Base URL:** `https://app.lettr.com/api/`
- **Official documentation:** [Schedule Email](https://docs.lettr.com/api-reference/emails/schedule-email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | yes | Sender email address. |
| `html` | body | `string` | yes | HTML email body. |
| `scheduled_at` | body | `string` | yes | Scheduled delivery timestamp. |
| `subject` | body | `string` | yes | Email subject line. |
| `to[]` | body | `array<string>` | yes | Recipient email addresses. |
