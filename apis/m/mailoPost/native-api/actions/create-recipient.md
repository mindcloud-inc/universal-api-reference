# Create Recipient with MailoPost

Creates a new recipient in a MailoPost list.

## Endpoint

- **Method:** `POST`
- **Path:** `/email/lists/:id/recipients`
- **Base URL:** `https://api.mailopost.ru/v1`
- **Official documentation:** [Create Recipient](https://mailopost.ru/api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | MailoPost recipient list identifier. |
| `email` | body | `string` | yes | Recipient email address. |
| `unconfirmed` | body | `boolean` | no | Create recipient as unconfirmed. |
| `values[]` | body | `array<object>` | no | Recipient parameter values. |
| `tags[]` | body | `array<string>` | no | Recipient tags. |
