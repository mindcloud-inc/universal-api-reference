# Update Message Webhook with MailoPost

Updates an existing message webhook in MailoPost.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/email/messages_webhooks/:id`
- **Base URL:** `https://api.mailopost.ru/v1`
- **Official documentation:** [Update Message Webhook](https://mailopost.ru/api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | MailoPost message webhook identifier. |
| `title` | body | `string` | no | Webhook title. |
| `url` | body | `string` | no | Webhook delivery URL. |
| `kinds[]` | body | `array<string>` | no | Message kinds for this webhook. |
| `events[]` | body | `array<string>` | no | Webhook events to subscribe to. |
| `status` | body | `string` | no | Webhook status. |
