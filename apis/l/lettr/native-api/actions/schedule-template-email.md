# Schedule Template Email with Lettr

## Endpoint

- **Method:** `POST`
- **Path:** `/emails/scheduled`
- **Base URL:** `https://app.lettr.com/api/`
- **Official documentation:** [Schedule Template Email](https://docs.lettr.com/api-reference/emails/schedule-email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | yes | Sender email address. |
| `scheduled_at` | body | `string` | yes | Scheduled delivery timestamp. |
| `substitution_data` | body | `object` | no | Template substitution variables. |
| `template_slug` | body | `string` | yes | Template slug for templated sends. |
| `to[]` | body | `array<string>` | yes | Recipient email addresses. |
