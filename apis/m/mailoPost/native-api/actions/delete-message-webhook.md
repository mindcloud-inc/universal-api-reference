# Delete Message Webhook with MailoPost

Deletes an existing message webhook from MailoPost.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/email/messages_webhooks/:id`
- **Base URL:** `https://api.mailopost.ru/v1`
- **Official documentation:** [Delete Message Webhook](https://mailopost.ru/api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | MailoPost message webhook identifier. |
