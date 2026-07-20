# Create Message Webhook with MailoPost

Creates a new message webhook in MailoPost.

## Endpoint

- **Method:** `POST`
- **Path:** `/email/messages_webhooks`
- **Base URL:** `https://api.mailopost.ru/v1`
- **Official documentation:** [Create Message Webhook](https://mailopost.ru/api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Webhook title. |
| `url` | body | `string` | yes | Webhook delivery URL. |
| `kinds[]` | body | `array<string>` | yes | Message kinds for this webhook. |
| `events[]` | body | `array<string>` | yes | Webhook events to subscribe to. |
