# Send Email Template Message with MailoPost

Sends an email from a MailoPost template.

## Endpoint

- **Method:** `POST`
- **Path:** `/email/templates/:template_id/messages`
- **Base URL:** `https://api.mailopost.ru/v1`
- **Official documentation:** [Send Email Template Message](https://mailopost.ru/api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | path | `string` | yes | MailoPost template identifier. |
| `to` | body | `string` | yes | Recipient email address. |
| `payment` | body | `string` | no | Billing mode for the template message. |
| `params` | body | `object` | no | Template substitution values. |
