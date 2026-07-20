# Send Post with talkSpirit

Creates a new post in talkSpirit via incoming webhook.

## Endpoint

- **Method:** `POST`
- **Path:** `{webhookUrl}`
- **Base URL:** `https://webhook.talkspirit.com`
- **Official documentation:** [Send Post](https://talkspirit.github.io/docs/incoming-webhooks/#sending-posts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | no | — |
| `content` | body | `string` | yes | — |
| `thread_id` | body | `string` | no | Optional thread identifier used to group related posts into the same discussion. |
| `url` | body | `string` | no | — |
| `contact` | body | `object` | no | — |
| `display_name` | body | `string` | no | — |
| `contact.url` | body | `string` | no | — |
| `contact.icon` | body | `string` | no | — |
