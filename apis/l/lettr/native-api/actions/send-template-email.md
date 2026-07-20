# Send Template Email with Lettr

## Endpoint

- **Method:** `POST`
- **Path:** `/emails`
- **Base URL:** `https://app.lettr.com/api/`
- **Official documentation:** [Send Template Email](https://docs.lettr.com/api-reference/emails/send-email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | yes | Sender email address. |
| `substitution_data` | body | `object` | no | Template substitution variables. |
| `template_slug` | body | `string` | yes | Template slug for templated sends. |
| `to[]` | body | `array<string>` | yes | Recipient email addresses. |
