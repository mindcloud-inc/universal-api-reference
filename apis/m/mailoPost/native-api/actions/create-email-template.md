# Create Email Template with MailoPost

Creates a new email template in MailoPost.

## Endpoint

- **Method:** `POST`
- **Path:** `/email/templates`
- **Base URL:** `https://api.mailopost.ru/v1`
- **Official documentation:** [Create Email Template](https://mailopost.ru/api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_email` | body | `string` | yes | Sender email address. |
| `from_name` | body | `string` | no | Sender display name. |
| `subject` | body | `string` | yes | Template subject line. |
| `name` | body | `string` | no | Template name. |
| `text` | body | `string` | no | Plain-text template body. |
| `html` | body | `string` | yes | HTML template body. |
| `preset_params[]` | body | `array<string>` | no | Template substitution parameter names. |
