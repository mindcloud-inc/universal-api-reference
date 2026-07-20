# Send Email with Engage

Sends a transactional email through Engage.

## Endpoint

- **Method:** `POST`
- **Path:** `/send/email`
- **Base URL:** `https://api.engage.so/v1`
- **Official documentation:** [Send Email](https://docs.engage.so/en-us/a/650f5a1ba36d1df032bd73aa-transactional-messaging#send-email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bcc[]` | body | `array<string>` | no | Email addresses for the blind carbon copy field. |
| `cc[]` | body | `array<string>` | no | Email addresses for the carbon copy field. |
| `reply_to` | body | `string` | no | Custom address that replies should go to. |
| `subject` | body | `string` | yes | The email subject. |
| `template` | body | `string` | no | Template name or identifier for a saved email template. |
| `template_variables` | body | `object` | no | Variables for the selected email template. |
| `text` | body | `string` | no | Alternative text version of the email content. |
| `track_clicks` | body | `boolean` | no | Set to true to enable click tracking. |
| `track_opens` | body | `boolean` | no | Set to true to enable open tracking. |
| `from.email` | body | `string` | yes | Sender email address. |
| `from.name` | body | `string` | yes | Sender name. |
| `to[]` | body | `array<string>` | yes | Recipient email address or addresses. |
| `html` | body | `string` | yes | HTML content of the email. |
