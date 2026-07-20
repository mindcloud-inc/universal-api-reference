# Bulk Cancel Messages with QStash

Cancels multiple messages in QStash by ID.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v2/messages`
- **Base URL:** `https://qstash-eu-central-1.upstash.io`
- **Official documentation:** [Bulk Cancel Messages](https://upstash.com/docs/qstash/api-refence/messages/bulk-cancel-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageIds[]` | query | `array<string>` | no | Specific message IDs to cancel. If provided, other filters are ignored. Send multiple values as a array. |
| `count` | query | `number` | no | Maximum number of messages to cancel. |
| `queueName` | query | `string` | no | Filter messages by queue name. |
| `url` | query | `string` | no | Filter messages by destination URL. |
| `label` | query | `string` | no | Filter messages by label. |
