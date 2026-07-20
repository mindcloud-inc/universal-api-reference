# List Cached Topic Messages with ntfy

Retrieves cached messages from an ntfy topic.

## Endpoint

- **Method:** `GET`
- **Path:** `/:topic/json`
- **Base URL:** `https://ntfy.sh`
- **Official documentation:** [List Cached Topic Messages](https://docs.ntfy.sh/subscribe/api/#fetch-cached-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `topic` | path | `string` | yes | The ntfy topic to read cached messages from. |
| `since` | query | `string` | no | Return cached messages since a timestamp, duration, or message ID. |
| `scheduled` | query | `boolean` | no | Include delayed or scheduled messages in the cached message list. |
| `id` | query | `string` | no | Only return the exact message ID. |
| `message` | query | `string` | no | Only return messages whose body exactly matches the given message. |
| `title` | query | `string` | no | Only return messages whose title exactly matches the given title. |
| `priority` | query | `string` | no | Only return messages that match any of the given priorities. Send multiple values as a string separated by `,`. |
| `tags` | query | `string` | no | Only return messages that contain all listed tags. Send multiple values as a string separated by `,`. |
